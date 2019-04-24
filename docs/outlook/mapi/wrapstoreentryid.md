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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325668"
---
# <a name="wrapstoreentryid"></a>WrapStoreEntryID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
ConVertit l'identificateur d'entrée interne d'une banque de messages en un identificateur d'entrée plus utilisable par le système de messagerie. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
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
  
> dans Masque de réindicateur des indicateurs. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI. 
    
 _szDLLName_
  
> dans Nom de la DLL du fournisseur de banque de messages. 
    
 _cbOrigEntry_
  
> dans Taille, en octets, de l'identificateur d'entrée d'origine de la Banque de messages. 
    
 _lpOrigEntry_
  
> dans Pointeur vers une structure [EntryID](entryid.md) qui contient l'identificateur d'entrée d'origine. 
    
 _lpcbWrappedEntry_
  
> remarquer Pointeur vers la taille, en octets, du nouvel identificateur d'entrée. 
    
 _lppWrappedEntry_
  
> remarquer Pointeur vers un pointeur vers une structure **EntryID** qui contient le nouvel identificateur d'entrée. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Un objet de banque de messages conserve un identificateur d'entrée interne qui est significatif uniquement pour les fournisseurs de services qui résident dans ce magasin de messages. Pour les autres composants de messagerie, MAPI fournit une version intégrée de l'identificateur d'entrée interne qui le rend reconnu comme appartenant à la Banque de messages. Les fournisseurs de services corésidents doivent toujours recevoir l'identificateur d'entrée d'origine de la Banque de messages déenveloppée; les applications clientes doivent toujours recevoir la version encapsulée, qui est ensuite utilisable n'importe où dans le domaine de messagerie et dans d'autres domaines. 
  
Un fournisseur de services peut encapsuler un identificateur d'entrée de banque de messages à l'aide de la fonction **WrapStoreEntryID** ou de la méthode [IMAPISupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md) , qui appelle la fonction **WrapStoreEntryID** . Le fournisseur doit encapsuler l'identificateur d'entrée lors de l'exposition de la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) de la Banque de messages ou de son écriture dans une section de profil, et lors de l'exposition de la **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) inspecteur. MAPI encapsule un identificateur d'entrée de banque de messages lors de la réponse à un appel [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) . 
  
Lorsqu'une application cliente transmet un identificateur d'entrée de magasin de messages encapsulé à MAPI, par exemple dans un appel [IMAPISession:: OpenEntry](imapisession-openentry.md) , MAPI détourne l'identificateur d'entrée avant de l'utiliser pour appeler une méthode de fournisseur telle que [IMSProvider:: Logon](imsprovider-logon.md) ou [ IMSProvider:: CompareStoreIDs](imsprovider-comparestoreids.md). 
  

