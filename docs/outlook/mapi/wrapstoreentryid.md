---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: Convertit l’identificateur d’entrée interne d’une boutique de messages en un identificateur d’entrée plus utilisable par le système de messagerie.
ms.openlocfilehash: 5898b621e0971f6cd3cd3a1d9e00cccd1d4a8f1c
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762556"
---
# <a name="wrapstoreentryid"></a>WrapStoreEntryID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Convertit l’identificateur d’entrée interne d’une boutique de messages en un identificateur d’entrée plus utilisable par le système de messagerie. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
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

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les chaînes sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
 _szDLLName_
  
> [in] Nom de la DLL du fournisseur de magasins de messages. 
    
 _cbOrigEntry_
  
> [in] Taille, en octets, de l’identificateur d’entrée d’origine pour la boutique de messages. 
    
 _lpOrigEntry_
  
> [in] Pointeur vers une structure [ENTRYID](entryid.md) qui contient l’identificateur d’entrée d’origine. 
    
 _lpcbWrappedEntry_
  
> [out] Pointeur vers la taille, en octets, du nouvel identificateur d’entrée. 
    
 _lppWrappedEntry_
  
> [out] Pointeur vers un pointeur vers une structure **ENTRYID** qui contient le nouvel identificateur d’entrée. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Un objet de magasin de messages conserve un identificateur d’entrée interne qui n’est significatif que pour les fournisseurs de services coresident avec cette magasin de messages. Pour les autres composants de messagerie, MAPI fournit une version wrapped de l’identificateur d’entrée interne qui la rend reconnaissable car elle appartient à la magasin de messages. Les fournisseurs de services Coresident doivent toujours se faire donner l’identificateur d’entrée de magasin de messages d’origine non enveloppé ; les applications clientes doivent toujours avoir la version wrapped, qui est ensuite utilisable n’importe où dans le domaine de messagerie et dans d’autres domaines. 
  
Un fournisseur de services peut encapsuler un identificateur d’entrée de magasin de messages à l’aide de la fonction **WrapStoreEntryID** ou de la méthode [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) , qui appelle la fonction **WrapStoreEntryID** . Le fournisseur doit encapsuler l’identificateur d’entrée lors de l’exposition de la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la boutique de messages ou de son écriture dans une section de profil, et lors de l’exposition de la propriété **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)). MAPI encapsule un identificateur d’entrée de magasin de messages lors de la réponse à un appel [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . 
  
Lorsqu’une application cliente transmet un identificateur d’entrée de magasin de messages enveloppé à MAPI, par exemple dans un appel [IMAPISession::OpenEntry](imapisession-openentry.md) , MAPI démasque l’identificateur d’entrée avant de l’utiliser pour appeler une méthode de fournisseur telle que [IMSProvider::Logon](imsprovider-logon.md) ou [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md). 
  

