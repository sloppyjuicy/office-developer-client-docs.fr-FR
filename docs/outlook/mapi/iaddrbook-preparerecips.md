---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: db1c23f33e604d6aafdd8a046566c7390c281ad8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339220"
---
# <a name="iaddrbookpreparerecips"></a>IAddrBook::PrepareRecips

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie. 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'entrée. L'indicateur suivant peut être défini:
    
MAPI_CACHE_ONLY
  
> Utilisez uniquement le carnet d'adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d'ouvrir la liste d'adresses globale (LAG) en mode Exchange mis en cache et d'accéder à une entrée de ce carnet d'adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d'adresses Exchange.
    
 _lpSPropTagArray_
  
> dans Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriété qui indiquent les propriétés, le cas échéant, qui nécessitent une mise à jour. Le paramètre _lpSPropTagArray_ peut être null. 
    
 _lpRecipList_
  
> dans Pointeur vers une structure [ADRLIST](adrlist.md) qui contient la liste des destinataires. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La liste des destinataires a été préparée.
    
## <a name="remarks"></a>Remarques

Les clients et les fournisseurs de services appellent la méthode **PrepareRecips** pour effectuer les opérations suivantes: 
  
- Assurez-vous que tous les destinataires dans le paramètre _lpRecipList_ ont des identificateurs d'entrée à long terme. 
    
- Assurez-vous que chaque destinataire dans le paramètre _lpRecipList_ a les propriétés répertoriées dans le paramètre _lpSPropTagArray_ et que ces propriétés apparaissent au début de la liste des destinataires. 
    
MAPI convertit les identificateurs d'entrée à court terme de chaque destinataire en identificateurs d'entrée à long terme. Si nécessaire, les identificateurs d'entrée à long terme des destinataires sont récupérés à partir du fournisseur de carnet d'adresses approprié et toutes les propriétés supplémentaires sont demandées.
  
Dans une entrée de destinataire individuelle, les propriétés demandées sont classées en premier, suivies par les propriétés qui étaient déjà présentes pour l'entrée. Si une ou plusieurs des propriétés demandées dans le paramètre _lpSPropTagArray_ ne sont pas gérées par le fournisseur de carnet d'adresses approprié, leurs types de propriétés seront définis sur PT_ERROR. Leurs valeurs de propriété sont définies sur MAPI_E_NOT_FOUND ou sur une autre valeur qui donne une raison plus spécifique pour laquelle les propriétés ne sont pas disponibles. Chaque structure [SPropValue](spropvalue.md) incluse dans le paramètre _lpRecipList_ doit être allouée séparément à l'aide des fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIAllocateMore](mapiallocatemore.md) afin qu'elle puisse être libérée individuellement. 
  
Pour plus d'informations sur PT_ERROR, consultez la rubrique [types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

