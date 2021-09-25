---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6d65a0103e86b89aa051c41a1597d0b2208aa33e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596140"
---
# <a name="imapisupportcreateoneoff"></a>IMAPISupport::CreateOneOff

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Crée un identificateur d’entrée pour une adresse unique.
  
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
  
> [in] Pointeur vers le nom complet du destinataire de la PR_DISPLAY_NAME **(** [PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Le  _paramètre lpszName_ peut être NULL. 
    
 _lpszAdrType_
  
> [in] Pointeur vers le type d’adresse (tel que FAX, SMTP ou X500) du destinataire. Le  _paramètre lpszAdrType_ ne peut pas être NULL. 
    
 _lpszAddress_
  
> [in] Pointeur vers l’adresse de messagerie du destinataire. Le  _paramètre lpszAddress_ ne peut pas être NULL. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui affecte le destinataire. Les indicateurs suivants peuvent être définies :
    
MAPI_SEND_NO_RICH_INFO 
  
> Le destinataire ne peut pas gérer le contenu des messages formatés. Si MAPI_SEND_NO_RICH_INFO est définie, MAPI définit la  propriété PR_SEND_RICH_INFO[(PidTagSendRichInfo)](pidtagsendrichinfo-canonical-property.md)du destinataire sur FALSE. Si MAPI_SEND_NO_RICH_INFO n’est pas définie, MAPI définit cette propriété sur TRUE, sauf si l’adresse de messagerie du destinataire pointée par  _lpszAddress_ est interprétée comme une adresse Internet. Dans ce cas, MAPI **définit** PR_SEND_RICH_INFO sur FALSE. 
    
MAPI_UNICODE 
  
> Le nom complet, le type d’adresse et l’adresse sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, ces chaînes sont au format ANSI.
    
 _lpcbEntryID_
  
> [out] Pointeur vers le nombre d’octets dans l’identificateur d’entrée pointé par _le paramètre lppEntryID._ 
    
 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée du destinataire unique.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’identificateur d’entrée unique a été créé avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::CreateOneOff** est implémentée pour tous les objets de prise en charge du fournisseur de services. Les fournisseurs de services appellent **CreateOneOff** pour créer un identificateur d’entrée pour un destinataire unique (un destinataire qui n’appartient à aucun des conteneurs des fournisseurs de carnet d’adresses actuellement chargés). 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque vous avez terminé d’utiliser l’identificateur d’entrée renvoyé par **CreateOneOff,** libérez la mémoire allouée pour l’identificateur d’entrée à l’aide de la fonction [MAPIFreeBuffer.](mapifreebuffer.md) 
  
## <a name="notes-to-transport-providers"></a>Remarques aux fournisseurs de transport

Prendre en charge le format TNEF (Transport Neutral Encapsulation Format) et utiliser la valeur de la propriété **PR_SEND_RICH_INFO** pour déterminer s’il faut utiliser le format TNEF lorsque vous transportez un message. Le fait de ne pas prendre en charge le format TNEF ou de ne pas envoyer de message dans ce format lorsqu’il est demandé peut être un problème pour les clients basés sur un formulaire ou les clients qui nécessitent des propriétés MAPI personnalisées. Cela est dû au fait que le TNEF est généralement utilisé pour envoyer des propriétés personnalisées pour des classes de message personnalisées. 
  
## <a name="see-also"></a>Voir aussi



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propriété canonique PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

