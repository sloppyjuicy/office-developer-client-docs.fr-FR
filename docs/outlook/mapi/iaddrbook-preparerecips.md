---
title: IAddrBookPrepareRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IAddrBook.PrepareRecips
api_type:
- COM
ms.assetid: d423f7b5-23b8-44dd-bca3-6590182dc42d
ms.openlocfilehash: 37af0f0fc9a13834385d373fac86bf5b1f2b8bc2
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373185"
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
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouverte. L’indicateur suivant peut être définie :
    
MAPI_CACHE_ONLY
  
> Utilisez uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d’ouvrir la liste d’adresses globale (LAL) en mode Exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur Exchange carnet d’adresses.
    
 _lpSPropTagArray_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriétés qui indiquent les propriétés, le cas contraire, qui nécessitent une mise à jour. Le  _paramètre lpSPropTagArray_ peut être NULL. 
    
 _lpRecipList_
  
> [in] Pointeur vers une structure [ADRLIST](adrlist.md) qui contient la liste des destinataires. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La liste des destinataires a été préparée avec succès.
    
## <a name="remarks"></a>Remarques

Les clients et les fournisseurs de services appellent **la méthode PrepareRecips** pour : 
  
- Assurez-vous que tous les destinataires du _paramètre lpRecipList_ ont des identificateurs d’entrée à long terme. 
    
- Assurez-vous que chaque destinataire du paramètre _lpRecipList_ possède les propriétés répertoriées dans le paramètre _lpSPropTagArray_ et que ces propriétés apparaissent au début de la liste des destinataires. 
    
MAPI convertit les identificateurs d’entrée à court terme de chaque destinataire en identificateurs d’entrée à long terme. Si nécessaire, les identificateurs d’entrée à long terme des destinataires sont extraits du fournisseur de carnet d’adresses approprié et toutes les propriétés supplémentaires sont demandées.
  
Dans une entrée de destinataire individuelle, les propriétés demandées sont d’abord ordre, suivies de toutes les propriétés déjà présentes pour l’entrée. Si une ou plusieurs des propriétés demandées dans le paramètre _lpSPropTagArray_ ne sont pas gérées par le fournisseur de carnet d’adresses approprié, leurs types de propriétés sont PT_ERROR. Leurs valeurs de propriété sont définies sur MAPI_E_NOT_FOUND ou sur une autre valeur qui donne une raison plus spécifique pour laquelle les propriétés ne sont pas disponibles. Chaque structure [SPropValue](spropvalue.md) incluse dans le paramètre _lpRecipList_ doit être allouée séparément à l’aide des fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIAllocateMore](mapiallocatemore.md) afin qu’elle puisse être libérée individuellement. 
  
Pour plus d’informations PT_ERROR, voir [Types de propriétés](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

