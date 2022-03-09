---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
ms.openlocfilehash: b3f5e7e0d91ed387b84fb4e85330ea00879290e2
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63368859"
---
# <a name="imapisupportexpandrecips"></a>IMAPISupport::ExpandRecips

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Complète la liste des destinataires d’un message, en développe des listes de distribution particulières.
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpMessage_
  
> [in] Pointeur vers le message dont la liste des destinataires doit être traitée.
    
 _lpulFlags_
  
> [out] Pointeur vers un masque de bits d’indicateurs qui contrôle le type de traitement qui se produit. Les indicateurs suivants peuvent être définies :
    
NEEDS_PREPROCESSING 
  
> Le message doit être prétraité avant d’être envoyé.
    
NEEDS_SPOOLER 
  
> Lepooler MAPI (plutôt que le fournisseur de transport auquel l’appelant est étroitement associé) doit envoyer le message.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La liste des destinataires du message a été traitée avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::ExpandRecips est** implémentée pour les objets de prise en charge du fournisseur de magasins de messages. Les fournisseurs de magasins de messages **appellent ExpandRecips** pour demander à MAPI d’effectuer les tâches suivantes : 
  
- Développez certaines listes de distribution personnelles pour les destinataires de leurs composants.
    
- Remplacez tous les noms d’affichage qui ont été modifiés par les noms d’origine.
    
- Marquez les entrées en double.
    
- Résolvez toutes les adresses à une seule adresse. 
    
- Vérifiez si le message doit être prétraité et, si c’est le cas, définissez l’indicateur pointé par  _lpulFlags_ sur NEEDS_PREPROCESSING. 
    
 **ExpandRecips développe toutes** les listes de distribution qui ont le type d’adresse de messagerie MAPIPDL. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **toujours ExpandRecips dans le** cadre du traitement de vos messages. Appelez **ExpandRecips l’un** des premiers appels dans l’implémentation de votre méthode [IMessage::SubmitMessage](imessage-submitmessage.md) . 
  
## <a name="see-also"></a>Voir aussi



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

