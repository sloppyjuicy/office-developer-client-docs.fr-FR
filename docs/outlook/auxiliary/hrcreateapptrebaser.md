---
title: HrCreateApptRebaser
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 265028b7-a583-f6ba-0214-5a4322f98f35
description: Initialise un objet IOlkApptRebaser à utiliser lors de la redéfinition des rendez-vous dans les calendriers Outlook.
ms.openlocfilehash: 33ad47d59ee2ca1b2461f730494f3466b9f8b54a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397540"
---
# <a name="hrcreateapptrebaser"></a><span data-ttu-id="7d7f3-103">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="7d7f3-103">HrCreateApptRebaser</span></span>

<span data-ttu-id="7d7f3-104">Initialise un objet [IOlkApptRebaser](iolkapptrebaser.md) à utiliser lors de la redéfinition des rendez-vous dans les calendriers Outlook.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-104">Initializes an [IOlkApptRebaser](iolkapptrebaser.md) object for use in rebasing appointments in Outlook calendars.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="7d7f3-105">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="7d7f3-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d7f3-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="7d7f3-106">Header file:</span></span>  <br/> |<span data-ttu-id="7d7f3-107">tzmovelib.h</span><span class="sxs-lookup"><span data-stu-id="7d7f3-107">tzmovelib.h</span></span>  <br/> |
|<span data-ttu-id="7d7f3-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="7d7f3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7d7f3-109">tzmovelib.dll</span><span class="sxs-lookup"><span data-stu-id="7d7f3-109">tzmovelib.dll</span></span>  <br/> |
|<span data-ttu-id="7d7f3-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="7d7f3-110">Called by:</span></span>  <br/> |<span data-ttu-id="7d7f3-111">Applications clientes MAPI</span><span class="sxs-lookup"><span data-stu-id="7d7f3-111">MAPI client applications</span></span>  <br/> |
|<span data-ttu-id="7d7f3-112">Type de pointeur :</span><span class="sxs-lookup"><span data-stu-id="7d7f3-112">Pointer type:</span></span>  <br/> |<span data-ttu-id="7d7f3-113">**LPHRCREATEAPPTREBASER**</span><span class="sxs-lookup"><span data-stu-id="7d7f3-113">**LPHRCREATEAPPTREBASER**</span></span> <br/> |
|<span data-ttu-id="7d7f3-114">Point d’entrée DLL :</span><span class="sxs-lookup"><span data-stu-id="7d7f3-114">DLL entry point:</span></span>  <br/> |<span data-ttu-id="7d7f3-115">**HrCreateApptRebaser@44**</span><span class="sxs-lookup"><span data-stu-id="7d7f3-115">**HrCreateApptRebaser@44**</span></span> <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="7d7f3-116">Param�tres</span><span class="sxs-lookup"><span data-stu-id="7d7f3-116">Parameters</span></span>

<span data-ttu-id="7d7f3-117">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7d7f3-117">_ulFlags_</span></span>
  
> <span data-ttu-id="7d7f3-118">[in] Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-118">[in] Required.</span></span> <span data-ttu-id="7d7f3-119">Un masque binaire composé des indicateurs utilisés pour contrôler comment redéfinir est effectuée.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-119">A bitmask of flags used to control how rebasing is performed.</span></span> <span data-ttu-id="7d7f3-120">Les indicateurs suivants peuvent être définies et sont définies dans tzmovelib.h :</span><span class="sxs-lookup"><span data-stu-id="7d7f3-120">The following flags can be set and are defined in tzmovelib.h:</span></span>
    
   - <span data-ttu-id="7d7f3-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** : éléments de rendez-vous dans laquelle l’utilisateur est l’organisateur de la réunion sont redéfinies.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-121">**REBASE_FLAG_UPDATE_ORGANIZED_MEETINGS** —Appointment items in which the user is the meeting organizer are rebased.</span></span> <span data-ttu-id="7d7f3-122">Notez que par défaut, cela entraîne Outlook pour envoyer des mises à jour de réunion à tous les participants à une réunion en cours redéfinie.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-122">Note that by default, this causes Outlook to send meeting updates to all attendees of any meeting being rebased.</span></span> <span data-ttu-id="7d7f3-123">Vous pouvez combiner cet indicateur avec **REBASE_FLAG_FORCE_NO_EX_UPDATES** ou **REBASE_FLAG_FORCE_NO_UPDATES** pour modifier le mode de gestion des mises à jour de la réunion.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-123">You can combine this flag with either **REBASE_FLAG_FORCE_NO_EX_UPDATES** or **REBASE_FLAG_FORCE_NO_UPDATES** to change how meeting updates are handled.</span></span> 
    
   - <span data-ttu-id="7d7f3-124">**REBASE_FLAG_UPDATE_UNMARKED** : mettre à jour des éléments de rendez-vous qui n’ont pas été marqués avec un fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-124">**REBASE_FLAG_UPDATE_UNMARKED** —Update appointment items that have not been marked with a time zone.</span></span> <span data-ttu-id="7d7f3-125">Si cet indicateur n’est spécifié, la valeur de *pTZMissing* est utilisée comme un élément est créé dans le fuseau horaire pour tous les éléments qui n’ont pas de données de fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-125">If this flag is specified, the  *pTZMissing*  value is used as the time zone that an item is created in for all items that do not have time zone data.</span></span> 
    
   - <span data-ttu-id="7d7f3-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** : mettre à jour uniquement les éléments de rendez-vous périodiques.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-126">**REBASE_FLAG_UPDATE_ONLYRECURRING** —Update only recurring appointment items.</span></span> 
    
   - <span data-ttu-id="7d7f3-127">**REBASE_FLAG_NO_UI** : ne pas afficher une interface utilisateur (IU), y compris les boîtes de dialogue d’ouverture de session sont généralement affichés lors de l’ouverture d’une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-127">**REBASE_FLAG_NO_UI** —Do not show any user interface (UI), including logon dialog boxes generally displayed when opening a message store.</span></span> 
    
   - <span data-ttu-id="7d7f3-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** : ne pas redéfinir des éléments de rendez-vous qui se produisent dans le passé.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-128">**REBASE_FLAG_UPDATE_MINIMIZEAPPTS** —Do not rebase appointment items that occur in the past.</span></span> 
    
   - <span data-ttu-id="7d7f3-129">**REBASE_FLAG_FORCE_REBASE** : ne pas vérifier l’organisateur pour redéfinir des décisions, mais redéfinir les éléments de rendez-vous dans laquelle l’utilisateur est un participant.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-129">**REBASE_FLAG_FORCE_REBASE** —Do not check the organizer for rebasing decisions, but rebase appointment items in which the user is an attendee.</span></span> 
    
   - <span data-ttu-id="7d7f3-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** — envoyer des mises à jour uniquement si l’utilisateur est l’organisateur et le destinataire n’est pas connecté à un serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-130">**REBASE_FLAG_FORCE_NO_EX_UPDATES** —Send updates only if the user is the organizer and recipient is not connected to an Exchange Server.</span></span> 
    
   - <span data-ttu-id="7d7f3-131">**REBASE_FLAG_FORCE_NO_UPDATES** : ne jamais envoyer des mises à jour.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-131">**REBASE_FLAG_FORCE_NO_UPDATES** —Never send updates.</span></span> 
    
   - <span data-ttu-id="7d7f3-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** — redéfinir uniquement les éléments de rendez-vous uniques créés avant le correctif a été appliqué.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-132">**REBASE_FLAG_ONLY_CREATED_PRE_PATCH** —Rebase only single-instance appointment items created before the patch was applied.</span></span> 
    
   - <span data-ttu-id="7d7f3-133">**REBASE_FLAG_REPORTING_MODE** : ne pas réellement rebase, rapport uniquement les éléments de rendez-vous qui doit être redéfini.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-133">**REBASE_FLAG_REPORTING_MODE** —Do not actually rebase, just report appointment items that would be rebased.</span></span> 
    
   - <span data-ttu-id="7d7f3-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** — envoie des mises à jour de réunion à des ressources.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-134">**REBASE_FLAG_SEND_RESOURCE_UPDATES** —Send meeting updates to resources.</span></span> 
    
<span data-ttu-id="7d7f3-135">_pSession_</span><span class="sxs-lookup"><span data-stu-id="7d7f3-135">_pSession_</span></span>
  
> <span data-ttu-id="7d7f3-136">[in] Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-136">[in] Required.</span></span> <span data-ttu-id="7d7f3-137">Pointeur vers une interface de session MAPI.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-137">A pointer to a MAPI session interface.</span></span>
    
<span data-ttu-id="7d7f3-138">_pCalendarMsgStore_</span><span class="sxs-lookup"><span data-stu-id="7d7f3-138">_pCalendarMsgStore_</span></span>
  
> <span data-ttu-id="7d7f3-139">[in] Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-139">[in] Required.</span></span> <span data-ttu-id="7d7f3-140">Pointeur vers une banque de messages contenant des éléments de rendez-vous à être redéfini.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-140">A pointer to a message store containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="7d7f3-141">_pCalendarFolder_</span><span class="sxs-lookup"><span data-stu-id="7d7f3-141">_pCalendarFolder_</span></span>
  
> <span data-ttu-id="7d7f3-142">[in] Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-142">[in] Required.</span></span> <span data-ttu-id="7d7f3-143">Pointeur vers un dossier de calendrier contenant des éléments de rendez-vous à être redéfini.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-143">A pointer to a calendar folder containing appointment items to be rebased.</span></span>
    
<span data-ttu-id="7d7f3-144">_pwszUpdatePrefix_</span><span class="sxs-lookup"><span data-stu-id="7d7f3-144">_pwszUpdatePrefix_</span></span>
  
> <span data-ttu-id="7d7f3-145">[in] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-145">[in] Optional.</span></span> <span data-ttu-id="7d7f3-146">Pointeur vers une chaîne contenant le préfixe à sur les demandes de réunion.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-146">A pointer to a string containing the prefix to be prepended on meeting requests.</span></span> <span data-ttu-id="7d7f3-147">Peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-147">May be NULL.</span></span>
    
<span data-ttu-id="7d7f3-148">_pftInstallDateUTC_</span><span class="sxs-lookup"><span data-stu-id="7d7f3-148">_pftInstallDateUTC_</span></span>
  
> <span data-ttu-id="7d7f3-149">[in] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-149">[in] Optional.</span></span> <span data-ttu-id="7d7f3-150">Date d’installation du correctif de fuseau horaire.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-150">The time zone patch install date.</span></span> <span data-ttu-id="7d7f3-151">Utilisé uniquement si l’indicateur **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** est défini.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-151">Used only if the **REBASE_FLAG_ONLY_CREATED_PRE_PATCH** flag is set.</span></span> 
    
<span data-ttu-id="7d7f3-152">_IExpansionDepth_</span><span class="sxs-lookup"><span data-stu-id="7d7f3-152">_IExpansionDepth_</span></span>
  
> <span data-ttu-id="7d7f3-153">[in] Facultatif.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-153">[in] Optional.</span></span> <span data-ttu-id="7d7f3-154">La profondeur d’extension lors de la distribution de développement des listes à exclure des destinataires connecté au serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-154">The expansion depth when expanding distribution lists to exclude recipients connected to Exchange Server.</span></span> <span data-ttu-id="7d7f3-155">Utilisé uniquement si l’indicateur **REBASE_FLAG_FORCE_NO_EX_UPDATES** est défini.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-155">Only used if the **REBASE_FLAG_FORCE_NO_EX_UPDATES** flag is set.</span></span> 
    
<span data-ttu-id="7d7f3-156">_pTZTo_</span><span class="sxs-lookup"><span data-stu-id="7d7f3-156">_pTZTo_</span></span>
  
> <span data-ttu-id="7d7f3-157">[in] Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-157">[in] Required.</span></span> <span data-ttu-id="7d7f3-158">Pointeur vers une structure **TZDEFINITION** décrivant le fuseau horaire à être redéfini à.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-158">A pointer to a **TZDEFINITION** structure describing the time zone to be rebased to.</span></span> <span data-ttu-id="7d7f3-159">**TZDEFINITION** est défini dans tzmovelib.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-159">**TZDEFINITION** is defined in tzmovelib.</span></span> 
    
<span data-ttu-id="7d7f3-160">pTZMissing</span><span class="sxs-lookup"><span data-stu-id="7d7f3-160">pTZMissing</span></span>
  
> <span data-ttu-id="7d7f3-161">[in] Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-161">[in] Required.</span></span> <span data-ttu-id="7d7f3-162">Pointeur vers une structure **TZDEFINITION** décrivant le fuseau horaire pour être déterminée automatiquement si les informations de fuseau horaire ne sont pas marquées sur un élément.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-162">A pointer to a **TZDEFINITION** structure describing the time zone to be assumed if time zone information is not stamped on an item.</span></span> <span data-ttu-id="7d7f3-163">Ne doit pas être NULL, mais uniquement si l’indicateur **REBASE_FLAG_UPDATE_UNMARKED** est défini.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-163">Must not be NULL, but only used if the **REBASE_FLAG_UPDATE_UNMARKED** flag is set.</span></span> 
    
<span data-ttu-id="7d7f3-164">_ppError_</span><span class="sxs-lookup"><span data-stu-id="7d7f3-164">_ppError_</span></span>
  
> <span data-ttu-id="7d7f3-165">[out] Pointeur vers un pointeur vers une structure **MAPIERROR** contenant des informations de version, composant et le contexte de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-165">[out] A pointer to a pointer to a **MAPIERROR** structure containing version, component, and context information for the error.</span></span> <span data-ttu-id="7d7f3-166">Peut être NULL si aucune information d’erreur étendue n’est souhaitée.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-166">Can be NULL if no extended error information is desired.</span></span> <span data-ttu-id="7d7f3-167">Gratuit avec [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="7d7f3-167">Free with [MAPIFreeBuffer](https://msdn.microsoft.com/library/9412594f-8acc-4c7e-a668-4ec1da0ad9cf%28Office.15%29.aspx).</span></span> 
    
<span data-ttu-id="7d7f3-168">_ppApptRebase_</span><span class="sxs-lookup"><span data-stu-id="7d7f3-168">_ppApptRebase_</span></span>
  
> <span data-ttu-id="7d7f3-169">[out] Pointeur vers un pointeur vers l’interface **IOlkApptRebaser** retournée.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-169">[out] A pointer to a pointer to the returned **IOlkApptRebaser** interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="7d7f3-170">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="7d7f3-170">Return values</span></span>

<span data-ttu-id="7d7f3-171">S_OK si l'appel a réussi ; dans le cas contraire, un code d'erreur.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-171">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7d7f3-172">Note</span><span class="sxs-lookup"><span data-stu-id="7d7f3-172">Remarks</span></span>

<span data-ttu-id="7d7f3-173">Lorsque vous utilisez [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) pour rechercher l’adresse de cette fonction dans tzmovelib.dll, spécifiez **HrCreateApptRebaser@44** comme nom de la procédure.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-173">When using [GetProcAddress](https://msdn.microsoft.com/library/a0d7fc09-f888-4f46-a571-d3719a627597%28Office.15%29.aspx) to look for the address of this function in tzmovelib.dll, specify **HrCreateApptRebaser@44** as the procedure name.</span></span> <span data-ttu-id="7d7f3-174">Tous les indicateurs sont valides en combinaison avec eux.</span><span class="sxs-lookup"><span data-stu-id="7d7f3-174">Not all of the flags are valid in combination with each other.</span></span> 
  
<span data-ttu-id="7d7f3-175">Pour plus d’informations sur les différentes options, voir la section « Glossaire des options de ligne de commande pour l’outil de mise à jour des données de fuseau horaire Outlook » dans [931667 de la base de connaissances : comment faire pour résoudre les modifications de fuseau horaire à l’aide de l’outil de mise à jour de données de fuseau horaire pour Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span><span class="sxs-lookup"><span data-stu-id="7d7f3-175">For more information about the various options, see the section "Glossary of command-line options for the Outlook Time Zone Data Update tool" in [KB 931667: How to address time zone changes by using the Time Zone Data Update Tool for Microsoft Office Outlook](https://support.microsoft.com/kb/931667/en-us).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7d7f3-176">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d7f3-176">See also</span></span>

- [<span data-ttu-id="7d7f3-177">À propos de la relocalisation des calendriers par programme à l'heure</span><span class="sxs-lookup"><span data-stu-id="7d7f3-177">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

