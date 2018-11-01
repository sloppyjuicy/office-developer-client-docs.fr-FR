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
ms.openlocfilehash: 1526ed54fd3773856b009c7c3570064f5a66df28
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594942"
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

 _Caractère_
  
> [in] Pointeur vers le nom complet du destinataire de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)). Le paramètre _le caractère_ peut être NULL. 
    
 _lpszAdrType_
  
> [in] Pointeur vers le type d’adresse du destinataire (telles que télécopie, SMTP ou X500). Le paramètre _lpszAdrType_ ne peut pas être NULL. 
    
 _lpszAddress_
  
> [in] Pointeur vers l’adresse de messagerie du destinataire. Le paramètre _lpszAddress_ ne peut pas être NULL. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs influençant le destinataire unique. Les indicateurs suivants peuvent être définis :
    
MAPI_SEND_NO_RICH_INFO 
  
> Le destinataire ne peut pas gérer le contenu des messages mis en forme. Si MAPI_SEND_NO_RICH_INFO est défini, MAPI définit la propriété du destinataire **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) sur FALSE. Si MAPI_SEND_NO_RICH_INFO n’est pas définie, MAPI définit cette propriété sur TRUE, sauf si l’adresse de messagerie du destinataire désigné par _lpszAddress_ est interprétée comme une adresse Internet. Dans ce cas, MAPI définit **PR_SEND_RICH_INFO** sur FALSE. 
    
MAPI_UNICODE 
  
> Le nom complet, le type d’adresse et l’adresse sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, ces chaînes sont au format ANSI.
    
 _lpcbEntryID_
  
> [out] Un pointeur vers le nombre d’octets de l’identificateur d’entrée indiqué par le paramètre _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Pointeur vers un pointeur vers l’identificateur d’entrée pour le destinataire unique.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’identificateur d’entrée unique a été créé avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::CreateOneOff** est implémentée pour tous les objets de prise en charge de fournisseur de service. Fournisseurs de services d’appel **CreateOneOff** pour créer un identificateur d’entrée pour un destinataire unique (un destinataire qui n’appartient pas à tous les conteneurs à partir des fournisseurs de carnet d’adresses actuellement chargée). 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Lorsque vous avez terminé à l’aide de l’identificateur d’entrée renvoyée par **CreateOneOff**, libérer de la mémoire allouée à l’identificateur d’entrée à l’aide de la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="notes-to-transport-providers"></a>Remarques pour les fournisseurs de Transport

Prend en charge le Transport Neutral Encapsulation Format TNEF () et la valeur de la propriété **PR_SEND_RICH_INFO** pour déterminer s’il faut utiliser le format TNEF lorsque vous un message de transport. Ne pas de prise en charge TNEF ou ne pas envoyer un message dans ce format, lorsqu’elle est demandée peut être un problème pour les clients basés sur les formulaires ou les clients qui requièrent des propriétés MAPI personnalisées. Il s’agit, car le format TNEF est généralement utilisé pour envoyer des propriétés personnalisées pour les classes de message personnalisées. 
  
## <a name="see-also"></a>Voir aussi



[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagDisplayName](pidtagdisplayname-canonical-property.md)
  
[Propriété canonique PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

