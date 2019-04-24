---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 105219fe430cd8746c3aa6cf5cd90629d5f72080
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316526"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Complète la liste de destinataires d'un message, en développant des listes de distribution particulières.
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpMessage_
  
> dans Pointeur vers le message dont la liste de destinataires doit être traitée.
    
 _lpulFlags_
  
> remarquer Pointeur vers un masque de des indicateurs qui contrôle le type de traitement qui se produit. Les indicateurs suivants peuvent être définis:
    
NEEDS_PREPROCESSING 
  
> Le message doit être prétraité avant d'être envoyé.
    
NEEDS_SPOOLER 
  
> Le spouleur MAPI (plutôt que le fournisseur de transport auquel l'appelant est étroitement couplé) doit envoyer le message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La liste des destinataires du message a été traitée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: ExpandRecips** est implémentée pour les objets de prise en charge du fournisseur de banque de messages. Les fournisseurs de banques de messages appellent **ExpandRecips** pour inviter MAPI à effectuer les tâches suivantes: 
  
- Développez certaines listes de distribution personnelle vers leurs destinataires de composants.
    
- Remplacez tous les noms d'affichage qui ont été modifiés par les noms d'origine.
    
- Marquez toutes les entrées en double.
    
- Résoudre toutes les adresses ponctuelles. 
    
- Vérifiez si le message doit être prétraité et, si c'est le cas, définissez l'indicateur désigné par _lpulFlags_ sur NEEDS_PREPROCESSING. 
    
 **ExpandRecips** développe toutes les listes de distribution dont le type d'adresse de messagerie est MAPIPDL. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez toujours **ExpandRecips** dans le cadre de votre traitement de message. Appelez **ExpandRecips** l'un des premiers appels dans votre implémentation de la méthode [IMessage: SubmitMessage](imessage-submitmessage.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

