---
title: Création d’un élément de tâche récurrente simple
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e9ee8865-0983-439e-8405-7946c5ec8762
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: be765915b729824b8c8b4209f125f354b02bad2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345471"
---
# <a name="create-a-simple-recurrent-task-item"></a>Création d’un élément de tâche récurrente simple

**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI peut être utilisé pour créer des éléments de tâche. Cette rubrique décrit comment créer un élément de tâche récurrente simple.
  
Pour plus d’informations sur la façon de télécharger, d’afficher et d’exécuter le code à partir de l’application MFCMAPI et du projet CreateOutlookItemsAddin référencés dans cette rubrique, voir Installer les exemples utilisés dans cette [section.](how-to-install-the-samples-used-in-this-section.md)

### <a name="to-create-a-task-item"></a>Pour créer un élément de tâche

1. Ouvrez une magasin de messages. Pour plus d’informations sur l’ouverture d’une magasin de messages, voir [Ouverture d’une magasin de messages.](opening-a-message-store.md)
    
2. Ouvrez le dossier Tâches dans la magasin de messages. Pour plus d’informations, **voir PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md)).
    
3. Appelez la [méthode IMAPIFolder::CreateMessage](imapifolder-createmessage.md) dans le dossier Tâches pour créer l’élément de tâche. 
    
4. Définissez **la propriété dispidTaskRecur** ([PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md)) et d’autres propriétés liées aux tâches requises pour créer une tâche périodique.
    
5. Enregistrez le nouvel élément de tâche.
    
La  `AddTask` fonction dans le fichier source Tasks.cpp du projet CreateOutlookItemsAddin illustre ces étapes. La fonction prend les paramètres de la boîte de dialogue Ajouter une tâche qui s’affiche lorsque vous cliquez sur Ajouter une tâche dans le menu Des addins de l’exemple `AddTask` d’application  MFCMAPI.   La fonction dans Tasks.cpp affiche la boîte de dialogue et transmet les valeurs de la boîte de dialogue  `DisplayAddTaskDialog` à la  `AddTask` fonction. La fonction n’est pas directement liée à la création d’un élément de tâche à l’aide de  `DisplayAddTaskDialog` MAPI, elle n’est donc pas répertoriée ici. 
  
> [!IMPORTANT]
> Le code de l’application MFCMAPI  ne garantit pas que  le dossier Tâches a été sélectionné lorsque vous cliquez sur la commande Ajouter une tâche dans le menu **Addins.** La création d’éléments de tâche dans un dossier autre que le dossier **Tâches** peut entraîner un comportement non définie. Assurez-vous que vous avez sélectionné le  dossier **Tâches** avant d’utiliser la commande Ajouter une tâche dans l’application MFCMAPI. 
  
La  `AddTask` fonction est répertoriée ci-dessous. Notez que le  _paramètre lpFolder_ transmis à la fonction est un pointeur vers une  `AddTask` interface [IMAPIFolder](imapifolderimapicontainer.md) qui représente le dossier dans lequel la nouvelle tâche est créée. Étant donné _le lpFolder_ qui représente une interface **IMAPIFolder,** le code appelle la méthode [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) La **méthode CreateMessage** renvoie un code de réussite et un pointeur vers un pointeur vers une interface **IMessage.** La plupart du code de fonction gère le travail de spécification des propriétés en préparation de l’appel de la méthode `AddTask` [IMAPIProp::SetProps.](imapiprop-setprops.md) Si l’appel à la méthode **SetProps** réussit, la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) est appelée pour valider les modifications dans le magasin et créer un élément de tâche. 
  
La  `AddTask` fonction définit un certain nombre de propriétés nommées. Pour plus d’informations sur les propriétés nommées et la façon dont elles sont créées, voir Utilisation de MAPI pour créer des Outlook [2007.](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx) Étant donné que les propriétés nommées utilisées pour les éléments de tâche occupent plusieurs jeux de propriétés, il est important de prendre soin de créer des paramètres à transmettre à la méthode [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) 
  
La fonction utilise la fonction d’aide pour créer une structure représentant une périodence de tâche pour définir la `AddTask` `BuildWeeklyTaskRecurrencePattern` propriété **dispidTaskRecur.** Pour plus d’informations sur la structure de périodence de la tâche, voir Propri t canonique  `BuildWeeklyTaskRecurrencePattern` [PidLidTaskRecurrence](pidlidtaskrecurrence-canonical-property.md) et Propri t canonique [PidLidRecurrencePattern](pidlidrecurrencepattern-canonical-property.md). 

Notez que bien qu’une grande variété de modèles de récurrence soit possible, la fonction crée uniquement une récurrence  `BuildWeeklyTaskRecurrencePattern` hebdomadaire. Il est également codé en dur pour un certain nombre d’hypothèses, telles que le type de calendrier (grégorien), le premier jour de la semaine (dimanche) et le nombre d’instances modifiées ou supprimées (aucune). Une fonction de création de modèle de récurrence à usage plus général doit accepter ces types de variables en tant que paramètres. 
  
Voici la liste complète de la  `AddTask` fonction. 
  
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

## <a name="see-also"></a>Voir aussi

- [Utilisation de MAPI pour créer Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

