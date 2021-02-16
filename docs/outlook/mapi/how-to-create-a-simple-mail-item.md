---
title: Création d’un élément de courrier simple
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bbf99c4b-3008-4475-a60a-648eaed59d01
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8b7afa8f3c04cb479906f721db8de90e8cf66f11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345192"
---
# <a name="create-a-simple-mail-item"></a>Création d’un élément de courrier simple
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI peut être utilisé pour créer et envoyer un message qui demande une réception de lecture. Lorsqu’une réception de lecture est demandée, le système de messagerie génère et renvoie un rapport de lecture à l’expéditeur lorsque le destinataire ouvre le message.
  
Pour plus d’informations sur la façon de télécharger, d’afficher et d’exécuter le code à partir de l’application MFCMAPI et du projet CreateOutlookItemsAddin référencés dans cette rubrique, voir Installer les exemples utilisés dans cette [section.](how-to-install-the-samples-used-in-this-section.md)


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a>Pour créer et envoyer un message demandant une réception de lecture

1. Créez un message sortant. Pour plus d’informations sur la création d’un message sortant, voir [Handling an Outgoing Message](handling-an-outgoing-message.md).
    
2. Ajoutez **la PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) et définissez-la sur **true**.
    
3. Ajoutez **la PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)).
    
4. Ajoutez **la PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)).
    
5. Envoyez le message en appelant [la méthode IMessage::SubmitMessage.](imessage-submitmessage.md) 
    
La  `AddMail` fonction dans le fichier source Mails.cpp du projet CreateOutlookItemsAddin illustre ces étapes. La fonction prend les paramètres de la boîte de dialogue Ajouter un message qui s’affiche lorsque vous cliquez sur la commande Ajouter un message dans le menu Des addins de l’exemple `AddMail` d’application  MFCMAPI.   La fonction dans Mails.cpp affiche la boîte de dialogue et transmet les valeurs de la boîte de dialogue  `DisplayAddMailDialog` à la  `AddMail` fonction. La fonction n’est pas directement liée à la création d’un élément de courrier à l’aide de  `DisplayAddMailDialog` MAPI, elle n’est donc pas répertoriée ici. La  `AddMail` fonction est répertoriée ci-dessous. 
  
Notez que le  _paramètre lpFolder_ transmis à la méthode est un pointeur vers une  `AddMail` interface [IMAPIFolder](imapifolderimapicontainer.md) qui représente le dossier dans lequel le nouveau message sera créé. Étant donné _le paramètre lpFolder_ qui représente une interface **IMAPIFolder,** le code appelle la méthode [IMAPIFolder::CreateMessage.](imapifolder-createmessage.md) La **méthode CreateMessage** renvoie un code de réussite et un pointeur vers un pointeur vers une interface [IMessage : IMAPIProp.](imessageimapiprop.md) 

La plupart du code de fonction gère le travail de définition des propriétés en préparation de l’appel de la méthode `AddMail` [IMAPIProp::SetProps.](imapiprop-setprops.md) Si l’appel à la méthode **SetProps** réussit, un appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) validera les modifications apportées au magasin et créera un nouvel élément de courrier. Ensuite, si nécessaire, la [méthode IMessage::SubmitMessage](imessage-submitmessage.md) est appelée pour envoyer le message. 
  
La `AddMail` fonction utilise deux fonctions d’aide  pour créer des valeurs pour PR_CONVERSATION_INDEX et **PR_REPORT_TAG** propriétés : les fonctions et les `BuildConversationIndex` `AddReportTag` fonctions. La fonction, située dans CreateOutlookItemsAddin.cpp, fait le même travail que la fonction  `BuildConversationIndex` MAPI [ScCreateConversationIndex](sccreateconversationindex.md) intégrée lorsqu’un index de conversation parent ne lui est pas transmis. Le format de la mémoire tampon d’index de conversation que ces fonctions génèrent est documenté dans la propriété canonique [PidTagConversationIndex.](pidtagconversationindex-canonical-property.md) 

La `AddReportTag` fonction, située dans Mails.cpp, appelle à son tour la fonction pour créer une `BuildReportTag` structure pour la propriété **PR_REPORT_TAG.** Pour plus d’informations sur la structure que la fonction crée, voir Propriété canonique  `BuildReportTag` [PidTagReportTag](pidtagreporttag-canonical-property.md).
  
Voici la liste complète de la  `AddMail` fonction. 
  
```cpp
HRESULT AddMail(LPMAPISESSION lpMAPISession,
            LPMAPIFOLDER lpFolder,
            LPWSTR szSubject, // PR_SUBJECT_W, PR_CONVERSATION_TOPIC
            LPWSTR szBody, // PR_BODY_W
            LPWSTR szRecipientName, // Recipient table
            BOOL bHighImportance, // PR_IMPORTANCE
            BOOL bReadReceipt, // PR_READ_RECEIPT_REQUESTED
            BOOL bSubmit,
            BOOL bDeleteAfterSubmit)
{
   if (!lpFolder) return MAPI_E_INVALID_PARAMETER;
   HRESULT hRes = S_OK;
   LPMESSAGE lpMessage = 0;
   // Create a message and set its properties
   hRes = lpFolder->CreateMessage(0,
      0,
      &lpMessage);
   if (SUCCEEDED(hRes))
   {
      // Because the properties to be set are known in advance, 
      // most of the structures involved can be statically declared 
      // to minimize expensive MAPIAllocateBuffer calls.
      SPropValue spvProps[NUM_PROPS] = {0};
      spvProps[p_PR_MESSAGE_CLASS_W].ulPropTag          = PR_MESSAGE_CLASS_W;
      spvProps[p_PR_ICON_INDEX].ulPropTag                 = PR_ICON_INDEX;
      spvProps[p_PR_SUBJECT_W].ulPropTag                = PR_SUBJECT_W;
      spvProps[p_PR_CONVERSATION_TOPIC_W].ulPropTag     = PR_CONVERSATION_TOPIC_W;
      spvProps[p_PR_BODY_W].ulPropTag                   = PR_BODY_W;
      spvProps[p_PR_IMPORTANCE].ulPropTag               = PR_IMPORTANCE;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].ulPropTag   = PR_READ_RECEIPT_REQUESTED;
      spvProps[p_PR_MESSAGE_FLAGS].ulPropTag             = PR_MESSAGE_FLAGS;
      spvProps[p_PR_MSG_EDITOR_FORMAT].ulPropTag         = PR_MSG_EDITOR_FORMAT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].ulPropTag         = PR_MESSAGE_LOCALE_ID;
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].ulPropTag = PR_INETMAIL_OVERRIDE_FORMAT;
      spvProps[p_PR_DELETE_AFTER_SUBMIT].ulPropTag      = PR_DELETE_AFTER_SUBMIT;
      spvProps[p_PR_INTERNET_CPID].ulPropTag            = PR_INTERNET_CPID;
      spvProps[p_PR_CONVERSATION_INDEX].ulPropTag         = PR_CONVERSATION_INDEX;
      spvProps[p_PR_MESSAGE_CLASS_W].Value.lpszW = L"IPM.Note";
      spvProps[p_PR_ICON_INDEX].Value.l = 0x103; // Unsent Mail
      spvProps[p_PR_SUBJECT_W].Value.lpszW = szSubject;
      spvProps[p_PR_CONVERSATION_TOPIC_W].Value.lpszW = szSubject;
      spvProps[p_PR_BODY_W].Value.lpszW = szBody;
      spvProps[p_PR_IMPORTANCE].Value.l = bHighImportance?IMPORTANCE_HIGH:IMPORTANCE_NORMAL;
      spvProps[p_PR_READ_RECEIPT_REQUESTED].Value.b = bReadReceipt?true:false;
      spvProps[p_PR_MESSAGE_FLAGS].Value.l = MSGFLAG_UNSENT;
      spvProps[p_PR_MSG_EDITOR_FORMAT].Value.l = EDITOR_FORMAT_PLAINTEXT;
      spvProps[p_PR_MESSAGE_LOCALE_ID].Value.l = 1033; // (en-us)
      spvProps[p_PR_INETMAIL_OVERRIDE_FORMAT].Value.l = NULL; // Mail system chooses default encoding scheme
      spvProps[p_PR_DELETE_AFTER_SUBMIT].Value.b = bDeleteAfterSubmit?true:false;
      spvProps[p_PR_INTERNET_CPID].Value.l = cpidASCII;
      hRes = BuildConversationIndex(
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.cb,
         &spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb);
      if (SUCCEEDED(hRes))
      {
         hRes = lpMessage->SetProps(NUM_PROPS, spvProps, NULL);
         if (SUCCEEDED(hRes))
         {
            hRes = AddRecipient(lpMAPISession,
               lpMessage,
               MAPI_TO,
               szRecipientName);
            AddInLog(true,L"CallMenu: AddRecipient - returned hRes = 0x%08X\n",hRes);
            if (SUCCEEDED(hRes))
            {
               if (bReadReceipt)
               {
                  hRes = AddReportTag(lpMessage);
               }
               if (SUCCEEDED(hRes))
               {
                  hRes = lpMessage->SaveChanges(KEEP_OPEN_READWRITE);
                  if (SUCCEEDED(hRes) && bSubmit)
                  {
                     hRes = lpMessage->SubmitMessage(NULL);
                  }
               }
            }
         }
      }
      if (spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb)
         delete[] spvProps[p_PR_CONVERSATION_INDEX].Value.bin.lpb;
   }
   if (lpMessage) lpMessage->Release();
   return hRes;
}
```

## <a name="see-also"></a>Voir aussi

- [Utilisation de MAPI pour créer des éléments Outlook 2007](https://msdn.microsoft.com/library/cc678348%28office.12%29.aspx)

