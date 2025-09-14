# Synastria Server API
Documentation of the native server API available on the client side.

Original document by Imevul: https://github.com/imevul/SynastriaCoreLib/blob/master/SynastriaAPI.md

# General
## Types

### CustomGameDataType
| Name              | Value |
|-------------------|-------|
| PERK_ACQUIRED     | 1     |
| PERK_LIMIT        | 2     |
| PERK_ACTIVE       | 3     |
| PERK_PROG         | 4     |
| PERK_TASKASSIGN1  | 6     |
| PERK_TASKASSIGN2  | 7     |
| PERK_TASKPARTY    | 9     |
| PERK_OPTIONS      | 10    |
| ATTUNE_HAS        | 11    |
| MYTHIC_SELECT     | 12    |
| RESOURCE_BANK     | 13    |
| RESOURCE_LAST     | 14    |
| ATTUNE_RANDOMPROP | 15    |

## Consts
| Name              | Value                            |
|-------------------|----------------------------------|
| MAX_ITEMID        | (current max itemId in the game) |

## Functions

### Custom_CacheHaveItems() -> 
### Custom_CalculateMapMarker() -> 
### Custom_ClearDressupFacing() -> 
### Custom_CreateDropdown() -> 
### Custom_CreateDropdownMask() -> 
### Custom_CreateFrame() -> 
### Custom_CreateFrameButton() -> 
### Custom_DoProfessionRecipe() -> 
### Custom_GetAllCustomFrames() -> 
### Custom_GetCurrentCursorItem() -> 
### Custom_GetCurrentZone() -> 
### Custom_GetCurrentZoneOur() -> 
### Custom_GetEntityExtraDataFloat() -> 
### Custom_GetEntityExtraDataInt() -> 
### Custom_GetGossipQuests() -> 
### Custom_GetHaveItems() -> 
### Custom_GetHighestLearnedSpell() -> 
### Custom_GetIdFromLink() -> 
### Custom_GetItemGuid() -> 
### Custom_GetItemIdFromName() -> 
### Custom_GetItemLinkBySlot() -> 
### Custom_GetItemQualityColor() -> 
### Custom_GetItemSelect() -> 
### Custom_GetItemSelectCount() -> 
### Custom_GetItemVars() -> 
### Custom_GetMapFilteredResults() -> 
### Custom_GetMapMarker() -> 
### Custom_GetMerchantItem() -> 
### Custom_GetProfessionRecipeFromCraftedItem() -> 
### Custom_GetProfessionRecipeInfo() -> 
### Custom_GetProfessionRecipeReagents() -> 
### Custom_GetProfessionRecipes() -> 
### Custom_GetQuestCanAccept() -> 
### Custom_GetQuestCompleted() -> 
### Custom_GetQuestData() -> 
### Custom_GetQuestFaction() -> 
### Custom_GetQuestName() -> 
### Custom_GetQuestReq() -> 
### Custom_GetTotalMapMarkerCount() -> 
### Custom_GetZoneName() -> 
### Custom_HasAcquiredItem() -> 
### Custom_HaveAnyRewardOfQuest() -> 
### Custom_Internal_SetResultFromUseContainerItem() -> 
### Custom_IsContainerItemSoulbound() -> 
### Custom_IsHaveItem() -> 
### Custom_IsItemEquipMgr() -> 
### Custom_IsItemSoulbound() -> 
### Custom_IsOnQuest() -> 
### Custom_IsPlayerNear() -> 
### Custom_LockItem() -> 
### Custom_RegisterForUseContainerItem() -> 
### Custom_SendQuestTrack() -> 
### Custom_SetDressupFacing() -> 
### Custom_SetEntityExtraDataFloat() -> 
### Custom_SetEntityExtraDataInt() -> 
### Custom_SetItemButton() -> 
### Custom_SetItemSelectFilter() -> 
### Custom_SetMapMarkerOption() -> 
### Custom_SetTradeSkillCustomFilter() -> 
### Custom_ThousandSeparator() -> 
### Custom_TranslateMapPosition() -> 
### Custom_UnlockItem() -> 
### Custom_UnregisterForUseContainerItem() -> 
### Custom_UpdateDropdown() -> 
### Custom_UpdateDropdownMask() -> 
### Custom_UpdateItemButton() -> 
### Custom_UpdateItemButtons() -> 
### Custom_ZoneContains() -> 
### CustomExtractItemBonus() -> 
### CustomExtractItemEnchant() ->
### CustomExtractItemId() -> 
### CustomGenerateDescription() -> 
### CustomGetClassColor() -> 
### CustomGetClassEnglishName() -> 
### CustomGetClassId() -> int
### CustomGetClassMask() -> mask
### CustomGetClipboard() -> 
### CustomGetRaceId() -> int
### CustomHasTeleport() -> bool
### CustomIsClass() -> bool
### CustomIsClassMask(mask) -> bool
### CustomMarkDo() -> 
### CustomSetClipboard() -> 
### CustomTeleportCoord() -> 
### CustomTeleportDo() -> 
### CustomTeleportName() -> string
### Debug_SetEnableZoneItemCache() -> 
### GetClassColorCustom() -> 
### GetCustomGameData(typeId, index) -> int|float
### GetCustomGameDataCount(typeId) -> int
### GetCustomGameDataIndex(typeId, index) -> int|string
### GetCustomGameDataString() -> 
### GetItemExtraCustom(itemId) -> nil|
### GetItemInfoCustom(itemId) -> ...|nil
### GetItemTagsCustom(itemId) -> int, ...
### HandleModifiedItemClick() -> 
### RaiseCustomEvent() ->
### RegisterForCustomEvent() ->
### SetCustomGameData() ->
### SetCustomGameDataString() ->
### UnregisterForCustomEvent() ->
### OpenWarp() -> 



### NotifyServer() ->
### TM_DEBUG_REFRESH() -> 
### _GetAllTooltipFrames() -> 
### GameTime_GetFormattedTime() -> 
### GameTime_GetLocalTime() -> 
### GetManagedEvironment() -> 
### SecureHandler_OnDragEvent() -> 
### UIDropdownMenu_CreateInfo() -> 
### SecureHandlerSetFrameRef() -> 
### ShowUIPanel() -> 
### HideUIPanel() -> 
### UIFrameFlash() -> 
### GetReadonlyRestrictedTable() -> 
### Blizzard_CombatLog_HasEvent() -> 
### UpdateTalentSpecNames() -> 
### TalentFrame_LoadUI() -> 
### GetTexCoordsForRole() -> 
### GetBackgroundTexCoordsForRole() -> 
### LFDQueueFrameTypeDropdown_Initialize() -> 
### LFDList_DefaultFilterFunction() -> 
### LFD_CURRENT_FILTER() -> 
### Blizzard_CombatLog_GenerateFullFlagList() -> 
### Blizzard_CombatLog_DisableEvent() -> 
### Blizzard_CombatLog_InitializeFilters() -> 
### MerchantFrame_ConfirmHighCostItem() -> 
### MerchantFrame_ConfirmExtendedItemCost() -> 
### GetSelectedTalentClassIndex() -> 
### AskBuyAccountSlot() -> 
### Blizzard_CombatLog_EnableEvent() -> 
### Blizzard_CombatLog_GenerateFullEventList() -> 
### Blizzard_CombatLog_MenuHelper() -> 
### () -> 
### () -> 














## Events
Important! Before defining any event handler function, you should store any existing reference and make sure you call it first thing in your function. Otherwise, other addons depending on said event will break!

### OnCustomGameData(typeId, id, prev, cur)
Called at the start of sending data to the client

### OnCustomGameDataFinish()
Called after the transaction is finished and all data is available

### OnCustomGameInit()
Called after initializing the custom data the first time, for example after login


# Attunables
## Tables
### ~~ItemAttuneSkip~~
Used to contain information about unattunable items

### ItemAttuneStats
Contains key/val pairs for attunable stats for an item. Note! Only populated after the attunement summary window has been opened, and is probably not intended for use.

### ItemAttuneOverwrite
Contains key/val pairs for stats gained for attunable weapons. Not always populated, and is probably not intended for use.

### ItemAttuneAffix
Contains all affixes, and a table with the stats they would grant

## Functions
### OpenAffixMgr() -> 

### UpdateAffixMgr() -> 

### CloseAffixMgr() -> 

### OpenAttuneMgr() -> 

### CloseAttuneMgr() -> 

### UpdateAttuneMgr() -> 

### OpenAttuneSummary()
Opens the attunement window. Note that the stats are not refreshed when the window is opened this way! To refresh the attunement stats, you have to use the spell

### CloseAttuneSummary() -> 

### UpdateAttuneSummary() -> 

### AppendItemAttuneOverwrite() ->

### AppendItemAttuneSkip() -> 

### CalculateAttunableAffixCount() -> 

### CalculateAttunableCount() -> 

### CalculateAttunedAffixCount() -> 

### CalculateAttunedCount() -> 

### CanAttuneItemHelper(itemId) -> int
Check if the item can be attuned by the current character, taking level, class, and armor proficiency into account

### CanAttuneItemHelperEx() -> 

### CreateAttunedPackedId() -> 

### CustomExtractItemAffix() -> 

### FindItemAffix() -> 

### GetAffixNameCustom() -> 

### GetAttuneAffixName(itemId, affixId) -> string
Returns the affix name

### GetAttuneOverwrite() -> 

### GetAttuneStatName(statId) -> string
Returns the name of a stat, given a statId

### GetHighestAttunePct() -> 

### GetInProgressAttuneKeys() -> 

### GetItemAffixMask(itemId) -> possibleMask1 (uint32), possibleMask2 (uint32), attunedMask1 (uint32), attunedMask2 (uint32), activeIndex (int)

### GetItemAttuneForge(itemid) -> int
Returns the attuned forge level for an itemid
1 = Titanforged, 2 = Warforged, 3 = Lightforged

### GetItemAttuneOverwrite(itemId) -> table { stat1type, stat1value }
Get a list of tables (key/val pairs) when attuning weapons

### GetItemAttuneProgress(itemid, affixid, titanforged) -> int
Returns the attunment progress for an itemId (optional affixId, optional titanforged)
1 = Titanforged, 2 = Warforged, 3 = Lightforged

### GetItemLinkAttuneProgress() -> 

### HasAttunedAnyVariantEx() -> 

### HasAttunedAnyVariantOfItem(itemId) -> bool

### HideAttuneTex() -> 

### HookAttuneTooltip() -> 

### ItemAttune_SortFunc() -> 

### IsAttunableBySomeone(itemId) -> bool
Check if the item can be attuned at all, ignoring class, level, etc.

### ReadAffixPick() -> 

### ShowAttuneTex() -> 



# Perks
(Still unconfirmed. Most are probably not intended for use)
## Data
### PerkMgrPoints
### PerkMgrReadOnly

## Tables
### GetPerkActive
### PerkMgrPerks
### PerkMgrSets
### PerkMgrTaskAll
### PerkMgrTaskHeader
### PerkMgrTaskStr
### SynergyPerks

## Functions
### OpenPerkMgr()
Opens the Perk manager window

### ClosePerkMgr() -> 

### UpdatePerkMgr() -> 

### ChangePerkOption() -> 

### GetPerkActive(perkId)

### GetPerkAcquired(perkId)

### GetPerkInfoInfo(perkId)

### GetPerkLimit(perkId)

### GetPerkOption(optionId) -> 

### GetPerkOptions(perkId)

### GetPerkOptionsInfo(perkId, optionId)

### GetPerkSynergy() -> 

### GetPerkTaskAssign1(perkId)

### GetPerkTaskAssign2(perkId)

### GetPerkTaskParty() -> 

### GetPerkTaskProg(perkId)

### SetPerkActive(perkId)

### ~~SetPerkOptions(perkId, options)~~
Do not use: Does nothing towards the server

### TogglePerkOption() -> 

### _addPerkSynergy() -> 



# Bounties
## Functions
### OpenBountyMenu() -> 

### CloseBountyMenu() -> 

### UpdateBountyMenu() -> 

### _OnBountyEvent() -> 

### HookBountyTooltip() -> 

### ShowBountyTex() -> 

### HideBountyTex() -> 

### BHCreated() -> 

### BHError() -> 

### BHResponse() -> 



# Item Hunt (Item Tracker)
## Data
### ITEMHUNT_MAX_TOOLTIP_MOREITEMS
### ITEMHUNT_MAX_TOOLTIP_MORESOURCES

## Functions
### OpenItemHunt() -> 

### CloseItemHunt() ->

### UpdateItemHunt() -> 

### ResetItemHunt() -> 

### Custom_AddTrackObjLoc() -> 

### Custom_ClearTrackObjLoc() -> 

### Custom_GetAllTrackObjLoc() -> 

### Custom_GetObjLoc() -> 

### Custom_GetObjLocVersion() -> 

### Custom_IsObjLocLoaded() -> 

### Custom_RemoveTrackObjLoc() -> 

### HookSourceTooltip() -> 

### IH_GetItemList() -> 

### IH_SetNewAlpha() -> 

### IH_SetOptions() -> 

### ItemLocFixupObjId() -> 

### ItemLocGetAllItemsInZone() -> 

### ItemLocGetObjAt() -> 

### ItemLocGetObjCount() -> 

### ItemLocGetSourceAt() -> 

### ItemLocGetSourceCount() -> 

### ItemLocGetSourcesCompacted() -> 

### ItemLocGetSourceSort() -> 

### ItemLocIsLoaded() -> 

### ItemLocItemIsInMultiZone() -> 

### ItemLocItemIsInZone() -> 

### ItemLocSetObjSort() -> 

### ItemLocSetSourceSort() -> 

### ItemLocSourceIsInZone() -> 

### UpdateIHOptions() -> 



# Loot Database
### OpenLootDb() -> 

### CloseLootDb() -> 

### UpdateLootDbOptions() -> 

### _createLootDbTooltip() -> 



# Autoloot
## Functions
### OpenLootFilter()

### CloseLootFilter()

### UpdateLootFilter()

### Custom_GetLootFilter() -> 

### Custom_GetLootFilterRule() -> 

### Custom_GetLootFilterRuleEntry() -> 

### Custom_LootFilterExport() -> 

### Custom_LootFilterExportRule() -> 

### Custom_LootFilterImport() -> 

### Custom_LootFilterImportRule() -> 

### Custom_LootFilterResetToDefault() -> 

### Custom_SetLootFilter() -> 

### Custom_SetLootFilterOptions() -> 

### Custom_SetLootFilterRule() -> 

### Custom_SetLootFilterRuleEnabled() -> 

### Custom_SetLootFilterRuleEntry() -> 

### CountEnabledLootRuleByName() -> 

### DisableLootRuleByName() -> 

### EnableLootRuleByName() ->



# Resource Bank
## Functions
### OpenResourceSummary()
Opens the Resource Bank window

### CloseResourceSummary()
Closes the Resource Bank window

### UpdateResourceSummary()
Updates the Resource Bank window



# Leaderboard
## Tables
### LBoardData

## Functions
### OpenLeaderboards() -> 

### CloseLeaderboards() -> 

### UpdateLeaderboards() -> 

### LBoardCallback() -> 

### OpenLeaderboardsTo() -> 

### ResetLBCache() -> 



# Prestige Class
## Functions
### CMCGetClassAt() -> 

### CMCGetClassCount() -> 

### CMCGetClassData() -> 

### CMCGetClassId() -> 

### CMCGetClassKey() -> 

### CMCGetClassMask() -> 

### CMCGetClassName() -> 

### CMCGetClassNameColor() -> 

### CMCGetClassNameFromPack() -> 

### CMCGetMultiClassEnabled() -> 

### CMCGetMyClassName() -> 

### CMCHasClass() -> 

### CMCSetSelectedTalents() -> 



# Currency Tracker
## Events
### BackpackTokenButton_OnClick() ->

### BackpackTokenFrame_IsShown() -> 

### BackpackTokenFrame_Update() -> 

### TokenButton_OnClick() -> 

### TokenButton_OnLoad() -> 

### TokenButtonLinkButton_OnClick() -> 

### TokenFrame_OnLoad() -> 

### TokenFrame_OnShow() -> 

### TokenFrame_Update() -> 

### TokenFrame_UpdatePopup() -> 

### TokenFramePopup_CloseIfHidden() -> 

## Functions
### GetNumWatchedTokens() -> 

### ManageBackpackTokenFrame() -> 



# Transmog
## Data
### DUMMY_TRANSMOG_ITEM
### MAX_TRANSMOG_SET

## Tables
### TRANSMOG_FACING
### TRANSMOG_OFFSET_HANDS
### TRANSMOG_OFFSET_RACEHEIGHT
### TRANSMOG_OFFSET_RACEX
### TRANSMOG_OFFSET_RACEZOOM
### TRANSMOG_OFFSET_SLOT

## Functions
### OpenTransmog() -> 

### CloseTransmog() -> 

### UpdateTransmogMenu() -> 

### ActivateTransmog() -> 

### Custom_FixupTransmogId() -> 

### Custom_GetTransmogEnchant() -> 

### Custom_GetTransmogItem() -> 

### Custom_TransmogExport() -> 

### GetActiveTransmog() -> 

### GetTransmogOffsets() -> 

### GetTransmogRaceIndex() -> 

### _TransmogCleanup() -> 