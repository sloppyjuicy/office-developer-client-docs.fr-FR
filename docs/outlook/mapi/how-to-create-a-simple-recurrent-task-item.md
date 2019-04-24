---
title: Création d’un élément de tâche récurrente simple
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e9ee8865-0983-439e-8405-7946c5ec8762
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: be765915b729824b8c8b4209f125f354b02bad2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345471"
---
# <a name="create-a-simple-recurrent-task-item"></a><span data-ttu-id="e73a9-103">Création d’un élément de tâche récurrente simple</span><span class="sxs-lookup"><span data-stu-id="e73a9-103">Create a simple recurrent task item</span></span>

<span data-ttu-id="e73a9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e73a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e73a9-105">MAPI peut être utilisé pour créer des éléments de tâche.</span><span class="sxs-lookup"><span data-stu-id="e73a9-105">MAPI can be used to create to create task items.</span></span> <span data-ttu-id="e73a9-106">Cette rubrique décrit comment créer un élément de tâche récurrente simple.</span><span class="sxs-lookup"><span data-stu-id="e73a9-106">This topic describes how to create a simple recurrent task item.</span></span>
  
<span data-ttu-id="e73a9-107">Pour plus d'informations sur le téléchargement, l'affichage et l'exécution du code à partir de l'application MFCMAPI et du projet CreateOutlookItemsAddin référencé dans cette rubrique, voir [installer les exemples utilisés dans cette section](how-to-install-the-samples-used-in-this-section.md).</span><span class="sxs-lookup"><span data-stu-id="e73a9-107">For information about how to download, view, and run the code from the MFCMAPI application and CreateOutlookItemsAddin project referenced in this topic, see [Install the Samples Used in This Section](how-to-install-the-samples-used-in-this-section.md).</span></span>

### <a name="to-create-a-task-item"></a><span data-ttu-id="e73a9-108">Pour créer un élément de tâche</span><span class="sxs-lookup"><span data-stu-id="e73a9-108">To create a task item</span></span>

1. <span data-ttu-id="e73a9-109">Ouvrez une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="e73a9-109">Open a message store.</span></span> <span data-ttu-id="e73a9-110">Pour plus d'informations sur l'ouverture d'une banque de messages, voir [ouverture d'une banque de messages](opening-a-message-store.md).</span><span class="sxs-lookup"><span data-stu-id="e73a9-110">For information on how to open a message store, see [Opening a Message Store](opening-a-message-store.md).</span></span>
    
2. <span data-ttu-id="e73a9-111">Ouvrez le dossier tâches dans la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="e73a9-111">Open the Tasks folder in the message store.</span></span> <span data-ttu-id="e73a9-112">Pour plus d'informations, voir **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e73a9-112">For more information, see **PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="e73a9-113">Appelez la méthode [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) sur le dossier tâches pour créer le nouvel élément de tâche.</span><span class="sxs-lookup"><span data-stu-id="e73a9-113">Call the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method on the Tasks folder to create the new task item.</span></span> 
    
4. <span data-ttu-id="e73a9-114">Définissez la propriété **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) et les autres propriétés liées à la tâche requises pour créer une tâche récurrente.</span><span class="sxs-lookup"><span data-stu-id="e73a9-114">Set the **dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) property and other task-related properties required to create a recurrent task.</span></span>
    
5. <span data-ttu-id="e73a9-115">Enregistrez la nouvelle tâche.</span><span class="sxs-lookup"><span data-stu-id="e73a9-115">Save the new task item.</span></span>
    
<span data-ttu-id="e73a9-116">La `AddTask` fonction dans le fichier source Tasks. cpp du projet CreateOutlookItemsAddin illustre ces étapes.</span><span class="sxs-lookup"><span data-stu-id="e73a9-116">The  `AddTask` function in the Tasks.cpp source file of the CreateOutlookItemsAddin project demonstrates these steps.</span></span> <span data-ttu-id="e73a9-117">La `AddTask` fonction prend les paramètres de la boîte de dialogue **Ajouter une tâche** qui s'affiche lorsque vous cliquez sur **Ajouter une tâche** dans le menu **AddIns** de l'exemple d'application MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="e73a9-117">The  `AddTask` function takes parameters from the **Add Task** dialog box that is displayed when you click **Add Task** on the **Addins** menu in the MFCMAPI sample application.</span></span> <span data-ttu-id="e73a9-118">La `DisplayAddTaskDialog` fonction dans Tasks. cpp affiche la boîte de dialogue et transmet les valeurs de la boîte `AddTask` de dialogue à la fonction.</span><span class="sxs-lookup"><span data-stu-id="e73a9-118">The  `DisplayAddTaskDialog` function in Tasks.cpp displays the dialog box and passes values from the dialog box to the  `AddTask` function.</span></span> <span data-ttu-id="e73a9-119">La `DisplayAddTaskDialog` fonction n'est pas directement liée à la création d'un élément de tâche à l'aide de MAPI; elle n'est donc pas répertoriée ici.</span><span class="sxs-lookup"><span data-stu-id="e73a9-119">The  `DisplayAddTaskDialog` function does not relate directly to creating a task item using MAPI, so it is not listed here.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="e73a9-120">Le code dans l'application MFCMAPI ne garantit pas que le dossier **tâches** a été sélectionné lorsque vous cliquez sur la commande **Ajouter une tâche** dans le menu **AddIns** .</span><span class="sxs-lookup"><span data-stu-id="e73a9-120">The code in the MFCMAPI application does not ensure that the **Tasks** folder has been selected when you click the **Add Task** command on the **Addins** menu.</span></span> <span data-ttu-id="e73a9-121">La création d'éléments de tâche dans un dossier autre que le dossier **tâches** peut entraîner un comportement non défini.</span><span class="sxs-lookup"><span data-stu-id="e73a9-121">Creating task items in a folder other than the **Tasks** folder can cause undefined behavior.</span></span> <span data-ttu-id="e73a9-122">Assurez-vous que vous avez sélectionné le dossier **tâches** avant d'utiliser la commande **Ajouter une tâche** dans l'application MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="e73a9-122">Make sure that you have selected the **Tasks** folder before using the **Add Task** command in the MFCMAPI application.</span></span> 
  
<span data-ttu-id="e73a9-123">La `AddTask` fonction est indiquée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e73a9-123">The  `AddTask` function is listed below.</span></span> <span data-ttu-id="e73a9-124">Notez que le paramètre _lpFolder_ transmis à la `AddTask` fonction est un pointeur vers une interface [IMAPIFolder](imapifolderimapicontainer.md) qui représente le dossier dans lequel la nouvelle tâche est créée.</span><span class="sxs-lookup"><span data-stu-id="e73a9-124">Note that the  _lpFolder_ parameter passed to the  `AddTask` function is a pointer to an [IMAPIFolder](imapifolderimapicontainer.md) interface that represents the folder where the new task is created.</span></span> <span data-ttu-id="e73a9-125">Étant donné le _lpFolder_ qui représente une interface **IMAPIFolder** , le code appelle la méthode [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="e73a9-125">Given the  _lpFolder_ that represents an **IMAPIFolder** interface, the code calls the [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) method.</span></span> <span data-ttu-id="e73a9-126">La méthode **CreateMessage** renvoie un code de réussite et un pointeur vers un pointeur vers une interface **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="e73a9-126">The **CreateMessage** method returns a success code and a pointer to a pointer to an **IMessage** interface.</span></span> <span data-ttu-id="e73a9-127">La plupart du `AddTask` code de la fonction gère le travail de spécification des propriétés en vue de l'appel de la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) .</span><span class="sxs-lookup"><span data-stu-id="e73a9-127">Most of the  `AddTask` function code handles the work of specifying properties in preparation for calling the [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> <span data-ttu-id="e73a9-128">Si l'appel à la méthode **SetProps** réussit, la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) est appelée pour valider les modifications apportées au magasin et créer un élément de tâche.</span><span class="sxs-lookup"><span data-stu-id="e73a9-128">If the call to the **SetProps** method succeeds, the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method is called to commit the changes to the store and create a new task item.</span></span> 
  
<span data-ttu-id="e73a9-129">La `AddTask` fonction définit un certain nombre de propriétés nommées.</span><span class="sxs-lookup"><span data-stu-id="e73a9-129">The  `AddTask` function sets a number of named properties.</span></span> <span data-ttu-id="e73a9-130">Pour plus d'informations sur les propriétés nommées et leur création, consultez la rubrique [utilisation de MAPI pour créer des éléments Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e73a9-130">For information about named properties and how they are created, see [Using MAPI to Create Outlook 2007 Items](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx).</span></span> <span data-ttu-id="e73a9-131">Étant donné que les propriétés nommées utilisées pour les éléments de tâche occupent plusieurs jeux de propriétés, vous devez prendre garde lors de la création de paramètres à transmettre à la méthode [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="e73a9-131">Because the named properties used for task items occupy multiple property sets, care must be taken when building parameters to pass to the [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) method.</span></span> 
  
<span data-ttu-id="e73a9-132">La `AddTask` fonction utilise la `BuildWeeklyTaskRecurrencePattern` fonction d'assistance pour créer une structure représentant une récurrence de tâche pour la définition de la propriété **dispidTaskRecur** .</span><span class="sxs-lookup"><span data-stu-id="e73a9-132">The  `AddTask` function uses the  `BuildWeeklyTaskRecurrencePattern` helper function to build a structure representing a task recurrence for setting the **dispidTaskRecur** property.</span></span> <span data-ttu-id="e73a9-133">Pour plus d'informations sur la structure de `BuildWeeklyTaskRecurrencePattern` périodicité des tâches générée par la fonction, voir [propriété canonique PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md) et [propriété canonique PidLidRecurrencePattern](pidlidrecurrencepattern-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="e73a9-133">For information on the task recurrence structure the  `BuildWeeklyTaskRecurrencePattern` function builds, see [PidLidTaskRecurrence Canonical Property](pidlidtaskrecurrence-canonical-property.md) and [PidLidRecurrencePattern Canonical Property](pidlidrecurrencepattern-canonical-property.md).</span></span> 

<span data-ttu-id="e73a9-134">Notez que même si un grand nombre de périodicités est possible, `BuildWeeklyTaskRecurrencePattern` la fonction ne génère qu'une périodicité hebdomadaire.</span><span class="sxs-lookup"><span data-stu-id="e73a9-134">Note that while a large variety of recurrence patterns are possible, the  `BuildWeeklyTaskRecurrencePattern` function only builds a weekly recurrence pattern.</span></span> <span data-ttu-id="e73a9-135">Il est également codé en dur pour un certain nombre d'hypothèses, telles que le type de calendrier (grégorien), le premier jour de la semaine (dimanche) et le nombre d'instances modifiées ou supprimées (aucun).</span><span class="sxs-lookup"><span data-stu-id="e73a9-135">It is also hard coded for a number of assumptions, such as the calendar type (Gregorian), the first day of the week (Sunday), and the number of modified or deleted instances (none).</span></span> <span data-ttu-id="e73a9-136">Une fonction de création de modèle de récurrence plus générale doit accepter ces types de variables comme paramètres.</span><span class="sxs-lookup"><span data-stu-id="e73a9-136">A more general purpose recurrence pattern creation function would need to accept these sorts of variables as parameters.</span></span> 
  
<span data-ttu-id="e73a9-137">Voici la liste complète de la `AddTask` fonction.</span><span class="sxs-lookup"><span data-stu-id="e73a9-137">The following is the complete listing of the  `AddTask` function.</span></span> 
  
```cpp
HRESULT AddTask(LPMAPIFOLDER lpFolder,
            SYSTEMTIME* lpstStart, // PidLidCommonEnd, PidLidTaskDueDate, PidLidTaskRecurrence
            SYSTEMTIME* lpstEnd, // PidLidTaskRecurrence
            SYSTEMTIME* lpstFirstDOW, // PidLidTaskRecurrence
            DWORD dwPeriod, // PidLidTaskRecurrence
            DWORD dwOccurrenceCount, // PidLidTaskRecurrence
            DWORD dwPatternTypeSpecific, // PidLidTaskRecurrence
            LPWSTR szSubject, // PR_SUBJECT_W
            LPWSTR szBody) // PR_BODY_W
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      MAPINAMEID  rgnmid[ulTaskProps];
      LPMAPINAMEID rgpnmid[ulTaskProps];
      LPSPropTagArray lpNamedPropTags = NULL;
      ULONG i = 0;
      for (i = 0 ; i < ulTaskProps ; i++)
      {
         if (i < ulFirstTaskProp)
            rgnmid[i].lpguid = (LPGUID)&PSETID_Common;
         else
            rgnmid[i].lpguid = (LPGUID)&PSETID_Task;
         rgnmid[i].ulKind = MNID_ID;
         rgnmid[i].Kind.lID = aulTaskProps[i];
         rgpnmid[i] = &rgnmid[i];
      }
      hRes = lpFolder->GetIDsFromNames(
         ulTaskProps,
         (LPMAPINAMEID*) &rgpnmid,
         NULL,
         &lpNamedPropTags);
      if (SUCCEEDED(hRes) && lpNamedPropTags)
      {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
         SPropValue spvProps[NUM_PROPS] = {0};
         spvProps[p_PidLidTaskMode].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskMode],PT_LONG);
         spvProps[p_PidLidCommonEnd].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidCommonEnd],PT_SYSTIME);
         spvProps[p_PidLidTaskStatus].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskStatus],PT_LONG);
         spvProps[p_PidLidPercentComplete].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidPercentComplete],PT_DOUBLE);
         spvProps[p_PidLidTaskState].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskState],PT_LONG);
         spvProps[p_PidLidTaskRecurrence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskRecurrence],PT_BINARY);
         spvProps[p_PidLidTaskDeadOccurrence].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskDeadOccurrence],PT_BOOLEAN);
         spvProps[p_PidLidTaskOwner].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskOwner],PT_UNICODE);
         spvProps[p_PidLidTaskFRecurring].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskFRecurring],PT_BOOLEAN);
         spvProps[p_PidLidTaskOwnership].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskOwnership],PT_LONG);
         spvProps[p_PidLidTaskAcceptanceState].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskAcceptanceState],PT_LONG);
         spvProps[p_PidLidTaskFFixOffline].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskFFixOffline],PT_BOOLEAN);
         spvProps[p_PidLidTaskDueDate].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskDueDate],PT_SYSTIME);
         spvProps[p_PidLidTaskComplete].ulPropTag
            = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[p_PidLidTaskComplete],PT_SYSTIME);
         spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag   = PR_MESSAGE_CLASS_W;
         spvProps[p_PR_ICON_INDEX].ulPropTag        = PR_ICON_INDEX;
         spvProps[p_PR_SUBJECT_W].ulPropTag         = PR_SUBJECT_W;
         spvProps[p_PR_MESSAGE_FLAGS].ulPropTag     = PR_MESSAGE_FLAGS;
         spvProps[p_PR_BODY_W].ulPropTag            = PR_BODY_W;
         spvProps[p_PidLidTaskMode].Value.l = tdmtNothing;
         SYSTEMTIME stStartUTC = {0};
         TzSpecificLocalTimeToSystemTime(NULL,lpstStart,&stStartUTC);
         SystemTimeToFileTime(&stStartUTC,&spvProps[p_PidLidCommonEnd].Value.ft);
         spvProps[p_PidLidTaskStatus].Value.l = tsvNotStarted;
         spvProps[p_PidLidPercentComplete].Value.dbl = 0.0;
         spvProps[p_PidLidTaskState].Value.l = tdsOWNNEW;
         spvProps[p_PidLidTaskDeadOccurrence].Value.b = false;
         spvProps[p_PidLidTaskOwner].Value.lpszW = L"Unknown";
         spvProps[p_PidLidTaskFRecurring].Value.b = true;
         spvProps[p_PidLidTaskOwnership].Value.l = tovNew;
         spvProps[p_PidLidTaskAcceptanceState].Value.l = tdvNone;
         spvProps[p_PidLidTaskFFixOffline].Value.b = true;
         SystemTimeToFileTime(lpstStart,&spvProps[p_PidLidTaskDueDate].Value.ft);
         spvProps[p_PidLidTaskComplete].Value.b = false;
         spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Task";
         spvProps[p_PR_ICON_INDEX].Value.l = 0x501; // Unassigned Recurring Task
         spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
         spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_READ;
         spvProps[p_PR_BODY_W].Value.lpszW = szBody;
         hRes = BuildWeeklyTaskRecurrencePattern(
            lpstStart,
            lpstEnd,
            lpstFirstDOW,
            dwPeriod,
            dwOccurrenceCount,
            dwPatternTypeSpecific,
            &spvProps[p_PidLidTaskRecurrence].Value.bin.cb,
            &spvProps[p_PidLidTaskRecurrence].Value.bin.lpb);
         if (SUCCEEDED(hRes))
         {
            hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
            if (SUCCEEDED(hRes))
            {
               hRes = lpMessage->SaveChanges(FORCE_SAVE);
            }
         }
         if (spvProps[p_PidLidTaskRecurrence].Value.bin.lpb)
            delete[] spvProps[p_PidLidTaskRecurrence].Value.bin.lpb;
      }
      MAPIFreeBuffer(lpNamedPropTags);
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}

```

## <a name="see-also"></a><span data-ttu-id="e73a9-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e73a9-138">See also</span></span>

- [<span data-ttu-id="e73a9-139">Utilisation de MAPI pour créer des éléments Outlook 2007</span><span class="sxs-lookup"><span data-stu-id="e73a9-139">Using MAPI to Create Outlook 2007 Items</span></span>](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

