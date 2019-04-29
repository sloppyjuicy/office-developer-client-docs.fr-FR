---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9571d51e01c2d58d9b8a9a913ba2c210ae0bd44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411994"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un identificateur d'entrée pour une adresse ponctuelle.
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Paramètres

 _lpszName_
  
> dans Pointeur vers le nom d'affichage du destinataire de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Le paramètre _lpszName_ peut être null. 
    
 _lpszAdrType_
  
> dans Pointeur vers le type d'adresse (par exemple, FAX, SMTP ou X500) du destinataire. Le paramètre _lpszAdrType_ ne peut pas être null. 
    
 _lpszAddress_
  
> dans Pointeur vers l'adresse de messagerie du destinataire. Le paramètre _lpszAddress_ ne peut pas être null. 
    
 _ulFlags_
  
> dans Masque de bits des indicateurs qui affecte le destinataire unique. Les indicateurs suivants peuvent être définis:
    
MAPI_SEND_NO_RICH_INFO 
  
> Le destinataire ne peut pas gérer le contenu du message mis en forme. Si MAPI_SEND_NO_RICH_INFO est défini, MAPI affecte la valeur FALSe à la propriété **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) du destinataire. Si MAPI_SEND_NO_RICH_INFO n'est pas défini, MAPI affecte à cette propriété la valeur TRUE sauf si l'adresse de messagerie du destinataire désignée par _lpszAddress_ est interprétée comme une adresse Internet. Dans ce cas, MAPI définit **PR_SEND_RICH_INFO** sur false. 
    
MAPI_UNICODE 
  
> Le nom complet, le type d'adresse et l'adresse sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, ces chaînes sont au format ANSI.
    
 _lpcbEntryID_
  
> remarquer Pointeur vers le nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lppEntryID_ . 
    
 _lppEntryID_
  
> remarquer Pointeur vers un pointeur vers l'identificateur d'entrée pour le destinataire isolé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'identificateur d'entrée unique a été créé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: CreateOneOff** est implémentée pour tous les objets de prise en charge du fournisseur de services. Les fournisseurs de services appellent **CreateOneOff** pour créer un identificateur d'entrée pour un destinataire unique (un destinataire qui n'appartient à aucun des conteneurs de l'un des fournisseurs de carnets d'adresses actuellement chargés). 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque vous avez terminé d'utiliser l'identificateur d'entrée retourné par **CreateOneOff**, libérez de la mémoire allouée à l'identificateur d'entrée à l'aide de la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="notes-to-transport-providers"></a>Remarques relatives aux fournisseurs de transport

Prendre en charge le format TNEF (Transport Neutral Encapsulation Format) et utiliser la valeur de la propriété **PR_SEND_RICH_INFO** pour déterminer s'il faut utiliser le format TNEF lorsque vous transférez un message. Le fait de ne pas prendre en charge TNEF ou d'envoyer un message dans ce format lorsqu'il est demandé peut être un problème pour les clients basés sur des formulaires ou les clients qui nécessitent des propriétés MAPI personnalisées. Cela est dû au fait que le format TNEF est généralement utilisé pour envoyer des propriétés personnalisées pour des classes de message personnalisées. 
  
## <a name="see-also"></a>Voir aussi



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propriété canonique PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

