---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Initialise un objet IOlkApptRebaser à utiliser lors de la relocalisation des rendez-vous dans les calendriers Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317611"
---
# <a name="hrcreateapptrebaser"></a><span data-ttu-id="2408f-103">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="2408f-103">HrCreateApptRebaser</span></span>

<span data-ttu-id="2408f-104">Initialise un objet [IOlkApptRebaser](iolkapptrebaser.md) à utiliser lors de la relocalisation des rendez-vous dans les calendriers Outlook.</span><span class="sxs-lookup"><span data-stu-id="2408f-104">Initializes an [IOlkApptRebaser](iolkapptrebaser.md) object for use in rebasing appointments in Outlook calendars.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2408f-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="2408f-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2408f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2408f-106">Header file:</span></span>  <br/> |<span data-ttu-id="2408f-107">tzmovelib. h</span><span class="sxs-lookup"><span data-stu-id="2408f-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="2408f-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="2408f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2408f-109">tzmovelib. dll</span><span class="sxs-lookup"><span data-stu-id="2408f-109">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="2408f-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="2408f-110">Called by:</span></span>  <br/> |<span data-ttu-id="2408f-111">Applications clientes MAPI</span><span class="sxs-lookup"><span data-stu-id="2408f-111">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="2408f-112">Type de pointeur:</span><span class="sxs-lookup"><span data-stu-id="2408f-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="2408f-113">**LPHRCREATEAPPTREBASER**</span><span class="sxs-lookup"><span data-stu-id="2408f-113">**LPHRCREATEAPPTREBASER**</span></span> <br/> |
|<span data-ttu-id="2408f-114">Point d'entrée de DLL:</span><span class="sxs-lookup"><span data-stu-id="2408f-114">DLL entry point:</span></span>  <br/> |<span data-ttu-id="2408f-115">**HrCreateApptRebaser @ 44**</span><span class="sxs-lookup"><span data-stu-id="2408f-115">**HrCreateApptRebaser@44**</span></span> <br/> |
   
```cpp
HRESULT HrCreateApptRebaser(  
    ULONG ulFlags, 
    IMAPISession *pSession, 
    IMsgStore *pCalendarMsgStore, 
    IMAPIFolder *pCalendarFolder, 
    LPCWSTR pwszUpdatePrefix, 
    const FILETIME *pftInstallDateUTC, 
    LONG lExpansionDepth, 
    const TZDEFINITION *pTZTo, 
    const TZDEFINITION *pTZMissing, 
    MAPIERROR **ppError, 
    IOlkApptRebaser **ppApptRebase); 

```

## <a name="parameters"></a><span data-ttu-id="2408f-116">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2408f-116">Parameters</span></span>

<span data-ttu-id="2408f-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2408f-117">_ulFlags_</span></span>
  
> <span data-ttu-id="2408f-118">[in] Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2408f-118">[in] Required.</span></span> <span data-ttu-id="2408f-119">Masque de des indicateurs utilisés pour contrôler la manière dont la relocalisation est effectuée.</span><span class="sxs-lookup"><span data-stu-id="2408f-119">A bitmask of flags used to control how rebasing is performed.</span></span> <span data-ttu-id="2408f-120">Les indicateurs suivants peuvent être définis et définis dans tzmovelib. h:</span><span class="sxs-lookup"><span data-stu-id="2408f-120">The following flags can be set and are defined in tzmovelib.h:</span></span>
    
   - <span data-ttu-id="2408f-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** : éléments de rendez-vous dans lesquels l'utilisateur est l'organisateur de la réunion qui est rebasé.</span><span class="sxs-lookup"><span data-stu-id="2408f-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —Appointment items in which the user is the meeting organizer are rebased.</span></span> <span data-ttu-id="2408f-122">Notez que, par défaut, Outlook envoie les mises à jour de réunion à tous les participants de toutes les réunions rebasés.</span><span class="sxs-lookup"><span data-stu-id="2408f-122">Note that by default, this causes Outlook to send meeting updates to all attendees of any meeting being rebased.</span></span> <span data-ttu-id="2408f-123">Vous pouvez associer cet indicateur à **REBASE_FLAG_FORCE_NO_EX_UPDATES** ou **REBASE_FLAG_FORCE_NO_UPDATES** pour modifier la façon dont les mises à jour de réunion sont gérées.</span><span class="sxs-lookup"><span data-stu-id="2408f-123">You can combine this flag with either **REBASE_FLAG_FORCE_NO_EX_UPDATES** or **REBASE_FLAG_FORCE_NO_UPDATES** to change how meeting updates are handled.</span></span> 
    
   - <span data-ttu-id="2408f-124">**REBASE_FLAG_UPDATE_UNMARKED** : mettre à jour les éléments de rendez-vous qui n'ont pas été marqués avec un fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="2408f-124">**REBASE_FLAG_UPDATE_UNMARKED** —Update appointment items that have not been marked with a time zone.</span></span> <span data-ttu-id="2408f-125">Si cet indicateur est spécifié, la valeur *pTZMissing* est utilisée comme le fuseau horaire dans lequel un élément est créé pour tous les éléments qui n'ont pas de données de fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="2408f-125">If this flag is specified, the  *pTZMissing*  value is used as the time zone that an item is created in for all items that do not have time zone data.</span></span> 
    
   - <span data-ttu-id="2408f-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** — mettre à jour uniquement les éléments de rendez-vous périodiques.</span><span class="sxs-lookup"><span data-stu-id="2408f-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —Update only recurring appointment items.</span></span> 
    
   - <span data-ttu-id="2408f-127">**REBASE_FLAG_NO_UI** : n'affiche pas d'interface utilisateur, y compris les boîtes de dialogue d'ouverture de session qui s'affichent généralement lors de l'ouverture d'une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="2408f-127">**REBASE_FLAG_NO_UI** —Do not show any user interface (UI), including logon dialog boxes generally displayed when opening a message store.</span></span> 
    
   - <span data-ttu-id="2408f-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** — ne rebasez pas les éléments de rendez-vous qui se produisent dans le passé.</span><span class="sxs-lookup"><span data-stu-id="2408f-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —Do not rebase appointment items that occur in the past.</span></span> 
    
   - <span data-ttu-id="2408f-129">**REBASE_FLAG_FORCE_REBASE** — ne pas vérifier l'organisateur pour les décisions de relocalisation, mais rebaser les éléments de rendez-vous dans lesquels l'utilisateur est un participant.</span><span class="sxs-lookup"><span data-stu-id="2408f-129">**REBASE_FLAG_FORCE_REBASE** —Do not check the organizer for rebasing decisions, but rebase appointment items in which the user is an attendee.</span></span> 
    
   - <span data-ttu-id="2408f-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** — envoyer les mises à jour uniquement si l'utilisateur est l'organisateur et si le destinataire n'est pas connecté à un serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="2408f-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —Send updates only if the user is the organizer and recipient is not connected to an Exchange Server.</span></span> 
    
   - <span data-ttu-id="2408f-131">**REBASE_FLAG_FORCE_NO_UPDATES** — ne jamais envoyer de mises à jour.</span><span class="sxs-lookup"><span data-stu-id="2408f-131">**REBASE_FLAG_FORCE_NO_UPDATES** —Never send updates.</span></span> 
    
   - <span data-ttu-id="2408f-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** — relocaliser uniquement les éléments de rendez-vous uniques créés avant l'application du correctif.</span><span class="sxs-lookup"><span data-stu-id="2408f-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —Rebase only single-instance appointment items created before the patch was applied.</span></span> 
    
   - <span data-ttu-id="2408f-133">**REBASE_FLAG_REPORTING_MODE** : ne rebasez pas réellement les éléments de rendez-vous qui seraient rebasés.</span><span class="sxs-lookup"><span data-stu-id="2408f-133">**REBASE_FLAG_REPORTING_MODE** —Do not actually rebase, just report appointment items that would be rebased.</span></span> 
    
   - <span data-ttu-id="2408f-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** — envoyer des mises à jour de réunion aux ressources.</span><span class="sxs-lookup"><span data-stu-id="2408f-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —Send meeting updates to resources.</span></span> 
    
<span data-ttu-id="2408f-135">_pSession_</span><span class="sxs-lookup"><span data-stu-id="2408f-135">_pSession_</span></span>
  
> <span data-ttu-id="2408f-136">[in] Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2408f-136">[in] Required.</span></span> <span data-ttu-id="2408f-137">Pointeur vers une interface de session MAPI.</span><span class="sxs-lookup"><span data-stu-id="2408f-137">A pointer to a MAPI session interface.</span></span>
    
<span data-ttu-id="2408f-138">_pCalendarMsgStore_</span><span class="sxs-lookup"><span data-stu-id="2408f-138">_pCalendarMsgStore_</span></span>
  
> <span data-ttu-id="2408f-139">[in] Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2408f-139">[in] Required.</span></span> <span data-ttu-id="2408f-140">Pointeur vers une banque de messages contenant des éléments de rendez-vous à rebaser.</span><span class="sxs-lookup"><span data-stu-id="2408f-140">A pointer to a message store containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="2408f-141">_pCalendarFolder_</span><span class="sxs-lookup"><span data-stu-id="2408f-141">_pCalendarFolder_</span></span>
  
> <span data-ttu-id="2408f-142">[in] Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2408f-142">[in] Required.</span></span> <span data-ttu-id="2408f-143">Pointeur vers un dossier de calendrier contenant des éléments de rendez-vous à rebaser.</span><span class="sxs-lookup"><span data-stu-id="2408f-143">A pointer to a calendar folder containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="2408f-144">_pwszUpdatePrefix_</span><span class="sxs-lookup"><span data-stu-id="2408f-144">_pwszUpdatePrefix_</span></span>
  
> <span data-ttu-id="2408f-145">[in] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="2408f-145">[in] Optional.</span></span> <span data-ttu-id="2408f-146">Pointeur vers une chaîne contenant le préfixe à ajouter au début des demandes de réunion.</span><span class="sxs-lookup"><span data-stu-id="2408f-146">A pointer to a string containing the prefix to be prepended on meeting requests.</span></span> <span data-ttu-id="2408f-147">Peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="2408f-147">May be NULL.</span></span>
    
<span data-ttu-id="2408f-148">_pftInstallDateUTC_</span><span class="sxs-lookup"><span data-stu-id="2408f-148">_pftInstallDateUTC_</span></span>
  
> <span data-ttu-id="2408f-149">[in] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="2408f-149">[in] Optional.</span></span> <span data-ttu-id="2408f-150">Date d'installation du correctif du fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="2408f-150">The time zone patch install date.</span></span> <span data-ttu-id="2408f-151">Utilisé uniquement si l'indicateur **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** est défini.</span><span class="sxs-lookup"><span data-stu-id="2408f-151">Used only if the **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** flag is set.</span></span> 
    
<span data-ttu-id="2408f-152">_IExpansionDepth_</span><span class="sxs-lookup"><span data-stu-id="2408f-152">_IExpansionDepth_</span></span>
  
> <span data-ttu-id="2408f-153">[in] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="2408f-153">[in] Optional.</span></span> <span data-ttu-id="2408f-154">Profondeur d'expansion lors de l'extension des listes de distribution pour exclure les destinataires connectés à Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="2408f-154">The expansion depth when expanding distribution lists to exclude recipients connected to Exchange Server.</span></span> <span data-ttu-id="2408f-155">Utilisé uniquement si l'indicateur **REBASE_FLAG_FORCE_NO_EX_UPDATES** est défini.</span><span class="sxs-lookup"><span data-stu-id="2408f-155">Only used if the **REBASE_FLAG_FORCE_NO_EX_UPDATES** flag is set.</span></span> 
    
<span data-ttu-id="2408f-156">_pTZTo_</span><span class="sxs-lookup"><span data-stu-id="2408f-156">_pTZTo_</span></span>
  
> <span data-ttu-id="2408f-157">[in] Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2408f-157">[in] Required.</span></span> <span data-ttu-id="2408f-158">Pointeur vers une structure **TZDEFINITION** décrivant le fuseau horaire à rebaser.</span><span class="sxs-lookup"><span data-stu-id="2408f-158">A pointer to a **TZDEFINITION** structure describing the time zone to be rebased to.</span></span> <span data-ttu-id="2408f-159">**TZDEFINITION** est défini dans tzmovelib.</span><span class="sxs-lookup"><span data-stu-id="2408f-159">**TZDEFINITION** is defined in tzmovelib.</span></span> 
    
<span data-ttu-id="2408f-160">pTZMissing</span><span class="sxs-lookup"><span data-stu-id="2408f-160">pTZMissing</span></span>
  
> <span data-ttu-id="2408f-161">[in] Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="2408f-161">[in] Required.</span></span> <span data-ttu-id="2408f-162">Pointeur vers une structure **TZDEFINITION** décrivant le fuseau horaire à supposer si les informations de fuseau horaire ne sont pas marquées sur un élément.</span><span class="sxs-lookup"><span data-stu-id="2408f-162">A pointer to a **TZDEFINITION** structure describing the time zone to be assumed if time zone information is not stamped on an item.</span></span> <span data-ttu-id="2408f-163">Ne doit pas être NULL, mais utilisé uniquement si l'indicateur **REBASE_FLAG_UPDATE_UNMARKED** est défini.</span><span class="sxs-lookup"><span data-stu-id="2408f-163">Must not be NULL, but only used if the **REBASE_FLAG_UPDATE_UNMARKED** flag is set.</span></span> 
    
<span data-ttu-id="2408f-164">_ppError_</span><span class="sxs-lookup"><span data-stu-id="2408f-164">_ppError_</span></span>
  
> <span data-ttu-id="2408f-165">remarquer Pointeur vers un pointeur vers une structure **MAPIERROR** contenant les informations de version, de composant et de contexte pour l'erreur.</span><span class="sxs-lookup"><span data-stu-id="2408f-165">[out] A pointer to a pointer to a **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="2408f-166">Peut être NULL si aucune information d'erreur étendue n'est souhaitée.</span><span class="sxs-lookup"><span data-stu-id="2408f-166">Can be NULL if no extended error information is desired.</span></span> <span data-ttu-id="2408f-167">Gratuit avec [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="2408f-167">Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span></span> 
    
<span data-ttu-id="2408f-168">_ppApptRebase_</span><span class="sxs-lookup"><span data-stu-id="2408f-168">_ppApptRebase_</span></span>
  
> <span data-ttu-id="2408f-169">remarquer Pointeur vers un pointeur vers l'interface **IOlkApptRebaser** renvoyée.</span><span class="sxs-lookup"><span data-stu-id="2408f-169">[out] A pointer to a pointer to the returned **IOlkApptRebaser** interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="2408f-170">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="2408f-170">Return values</span></span>

<span data-ttu-id="2408f-171">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="2408f-171">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2408f-172">Remarques</span><span class="sxs-lookup"><span data-stu-id="2408f-172">Remarks</span></span>

<span data-ttu-id="2408f-173">Lors de l'utilisation de [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) pour Rechercher l'adresse de cette fonction dans tzmovelib. dll, spécifiez **HrCreateApptRebaser @ 44** comme nom de procédure.</span><span class="sxs-lookup"><span data-stu-id="2408f-173">When using [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) to look for the address of this function in tzmovelib.dll, specify **HrCreateApptRebaser@44** as the procedure name.</span></span> <span data-ttu-id="2408f-174">Les indicateurs ne sont pas tous valides les uns avec les autres.</span><span class="sxs-lookup"><span data-stu-id="2408f-174">Not all of the flags are valid in combination with each other.</span></span> 
  
<span data-ttu-id="2408f-175">Pour plus d'informations sur les différentes options, voir la section «Glossaire des options de ligne de commande pour l'outil de mise à jour des données de fuseau horaire Outlook» dans l' [article KB 931667: How to address Time Zone Changes by using the Time fuseau Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span><span class="sxs-lookup"><span data-stu-id="2408f-175">For more information about the various options, see the section "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2408f-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2408f-176">See also</span></span>

- [<span data-ttu-id="2408f-177">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="2408f-177">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

