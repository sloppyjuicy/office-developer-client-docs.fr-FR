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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2e41701d3a739864b1eafc8001833b7df5c8908b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783991"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**S’applique à**: Outlook 
  
Termine la liste des destinataires d’un message, développer des listes de distribution particulier.
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpMessage_
  
> [in] Pointeur vers le message qui contient la liste des destinataires à traiter.
    
 _lpulFlags_
  
> [out] Pointeur vers un masque de bits d’indicateurs qui contrôle le type de traitement qui se produit. Les indicateurs suivants peuvent être définis :
    
NEEDS_PREPROCESSING 
  
> Le message doit être prétraités avant son envoi.
    
NEEDS_SPOOLER 
  
> Le spouleur MAPI (plutôt que le fournisseur de transport dans lequel l’appelant est étroitement) doit envoyer le message.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Liste des destinataires du message a été correctement traitée.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::ExpandRecips** est implémentée pour les objets de prise en charge de fournisseur de magasin de message. Fournisseurs de magasins message appeler **ExpandRecips** pour demander l’interface MAPI pour effectuer les tâches suivantes : 
  
- Développez certaines listes de distribution personnelles aux destinataires d’un composant.
    
- Remplacez tous les noms complets qui ont été modifiées par les noms d’origine.
    
- Marquer des entrées en double.
    
- Résoudre toutes les adresses uniques. 
    
- Vérifier si le message a besoin de prétraitement et, si c’est le cas, définie l’indicateur désignés par _lpulFlags_ à NEEDS_PREPROCESSING. 
    
 **ExpandRecips** développe des listes de distribution dont le type de MAPIPDL adresse de messagerie. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Appelez toujours **ExpandRecips** dans le cadre de votre processus de message. Émettre un appel à **ExpandRecips** 1 de l’appelle d’abord dans votre implémentation de la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

