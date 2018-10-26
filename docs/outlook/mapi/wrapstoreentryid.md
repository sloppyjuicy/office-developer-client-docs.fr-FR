---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 45263396e69852a9ae17ff6fce284663bdf2fb07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585135"
---
# <a name="wrapstoreentryid"></a>WrapStoreEntryID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Convertit un identificateur d’entrée plus conviviaux identificateur d’entrée interne d’une banque de messages par le système de messagerie. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
WrapStoreEntryID(
  ULONG ulFlags,
  LPSTR szDLLName,
  ULONG cbOrigEntry,
  LPENTRYID lpOrigEntry,
  ULONG * lpcbWrappedEntry,
  LPENTRYID * lppWrappedEntry
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _szDLLName_
  
> [in] Nom de la DLL du fournisseur de banque de messages. 
    
 _cbOrigEntry_
  
> [in] Taille, en octets, de l’identificateur d’entrée d’origine pour la banque de messages. 
    
 _lpOrigEntry_
  
> [in] Pointeur vers une structure [ENTRYID](entryid.md) qui contient l’identificateur d’entrée d’origine. 
    
 _lpcbWrappedEntry_
  
> [out] Pointeur vers la taille, en octets, de l’identificateur d’entrée. 
    
 _lppWrappedEntry_
  
> [out] Pointeur vers un pointeur vers une structure **ENTRYID** qui contient l’identificateur d’entrée. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Objet store message conserve un identificateur d’entrée interne qui est uniquement explicite pour coresident de fournisseurs de service avec cette banque d’informations. Pour les autres composants de messagerie MAPI fournit une version renvoyé à la ligne de l’identificateur d’entrée interne qui rend reconnaissable qui appartiennent à la banque de messages. Fournisseurs de services coresident doivent toujours être donnés à l’identificateur d’entrée non message magasin d’origine ; applications clientes doivent toujours être données à la version encapsulée, qui est alors utilisable n’importe où dans le domaine de messagerie et dans d’autres domaines. 
  
Un fournisseur de services peut renvoyer un identificateur d’entrée de magasin de message à l’aide de la fonction **WrapStoreEntryID** ou la méthode [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) , qui appelle la fonction **WrapStoreEntryID** . Le fournisseur doit encapsuler l’identificateur d’entrée lors de l’exposition **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la banque de messages propriété ou l’écriture dans une section de profil et lors de l’exposition de la **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) propriété. MAPI encapsule un identificateur d’entrée de magasin de message lors de la réponse à un appel [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . 
  
Lorsqu’une application cliente transmet un identificateur d’entrée de magasin de message encapsulé à MAPI, par exemple dans un appel [IMAPISession::OpenEntry](imapisession-openentry.md) , MAPI Désencapsule l’identificateur d’entrée avant de les utiliser pour appeler une méthode de fournisseur telles que [IMSProvider::Logon](imsprovider-logon.md) ou [ IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md). 
  

