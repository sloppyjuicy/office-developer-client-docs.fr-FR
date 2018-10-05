---
title: Créer un élément de courrier simple
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bbf99c4b-3008-4475-a60a-648eaed59d01
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8b7afa8f3c04cb479906f721db8de90e8cf66f11
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401453"
---
# <a name="create-a-simple-mail-item"></a>Créer un élément de courrier simple
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
MAPI peut être utilisé pour créer et envoyer un message qui demande une confirmation de lecture. Si une confirmation de lecture est demandée, le système de messagerie génère et renvoie un rapport de lecture à l’expéditeur lorsque le destinataire ouvre le message.
  
Pour plus d’informations sur la façon de télécharger, afficher et exécuter le code de l’application de MFCMAPI et d’un projet CreateOutlookItemsAddin référencé dans cette rubrique, consultez [installer les exemples utilisés dans cette Section](how-to-install-the-samples-used-in-this-section.md).


### <a name="to-create-and-send-a-message-requesting-a-read-receipt"></a>Pour créer et envoyer un message de demande une confirmation de lecture

1. Créer un message sortant. Pour plus d’informations sur la création d’un message sortant, voir [Gestion d’un Message sortant](handling-an-outgoing-message.md).
    
2. Ajoutez la propriété **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) et la valeur **true**.
    
3. Ajoutez la propriété **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)).
    
4. Ajoutez la propriété **PR_REPORT_TAG** ([PidTagReportTag](pidtagreporttag-canonical-property.md)).
    
5. Envoyer le message en appelant la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) . 
    
Le `AddMail` fonction dans le fichier source Mails.cpp du projet CreateOutlookItemsAddin illustre ces étapes. Le `AddMail` fonction prend des paramètres à partir de la boîte de dialogue **Ajouter une messagerie** qui s’affiche lorsque vous cliquez sur la commande **Ajouter la messagerie** dans le menu **compléments** dans l’exemple d’application MFCMAPI. Le `DisplayAddMailDialog` fonction dans Mails.cpp affiche la boîte de dialogue et transmet les valeurs à partir de la boîte de dialogue à la `AddMail` fonction. Le `DisplayAddMailDialog` fonction n’est pas liée directement à la création d’un élément de courrier à l’aide de MAPI, il n’est pas répertorié ici. Le `AddMail` fonction est répertoriée ci-dessous. 
  
Notez que le paramètre _lpFolder_ transmis à la `AddMail` méthode est un pointeur vers une interface [IMAPIFolder](imapifolderimapicontainer.md) qui représente le dossier dans lequel le nouveau message sera créé. Étant donné le paramètre _lpFolder_ qui représente une interface **IMAPIFolder** , le code appelle la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . La méthode **CreateMessage** renvoie un code de réussite et un pointeur vers un pointeur vers une [IMessage : IMAPIProp](imessageimapiprop.md) interface. 

La plupart de la `AddMail` gère le code de la fonction de la définition de propriétés dans la préparation pour appeler la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) . Si l’appel à la méthode **SetProps** réussit, un appel à la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) valide les modifications dans le magasin et crée un nouvel élément de messagerie. Ensuite, si nécessaire, la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) est appelée pour envoyer le message. 
  
Le `AddMail` fonction utilise deux fonctions d’assistance pour générer des valeurs pour les propriétés **PR_CONVERSATION_INDEX** et **PR_REPORT_TAG** : le `BuildConversationIndex` et `AddReportTag` fonctions. Le `BuildConversationIndex` fonction, située dans CreateOutlookItemsAddin.cpp, effectue le travail de même que la fonction intégrée de MAPI [ScCreateConversationIndex](sccreateconversationindex.md) lorsqu’un index de conversation parent n’est pas transmis à celui-ci. Le format de la mémoire tampon index de conversation qui génèrent de ces fonctions est documenté dans la [Propriété canonique PidTagConversationIndex](pidtagconversationindex-canonical-property.md). 

Le `AddReportTag` fonction, située dans Mails.cpp, à son tour appelle la `BuildReportTag` fonction pour créer une structure de la propriété **PR_REPORT_TAG** . Pour plus d’informations sur la structure qui le `BuildReportTag` versions de fonction, voir [Propriété canonique PidTagReportTag](pidtagreporttag-canonical-property.md).
  
Voici la liste complète de la `AddMail` fonction. 
  
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

