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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 004498ac94aadaa075d87d4dd3c675c8cd5f4feb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563876"
---
# <a name="iaddrbookpreparerecips"></a>IAddrBook::PrepareRecips

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Prépare une liste de destinataires pour une utilisation ultérieure par le système de messagerie. 
  
```cpp
HRESULT PrepareRecips(
  ULONG ulFlags,
  LPSPropTagArray lpSPropTagArray,
  LPADRLIST lpRecipList
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’entrée est ouvert. Vous pouvez définir l’indicateur suivant :
    
MAPI_CACHE_ONLY
  
> Utilisez uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour autoriser une application cliente pour ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans le trafic entre le client et le serveur de création. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.
    
 _lpSPropTagArray_
  
> [in] Un pointeur vers une structure [SPropTagArray](sproptagarray.md) qui contient un tableau de balises de propriétés qui indiquent les propriétés, le cas échéant, qui nécessitent la mise à jour. Le paramètre _lpSPropTagArray_ peut être NULL. 
    
 _lpRecipList_
  
> [in] Pointeur vers une structure [ADRLIST](adrlist.md) qui contient la liste des destinataires. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La liste de destinataires a été correctement préparée.
    
## <a name="remarks"></a>Remarques

Clients et fournisseurs de services appellent la méthode **PrepareRecips** pour effectuer les opérations suivantes : 
  
- Assurez-vous que tous les destinataires dans le paramètre _lpRecipList_ ont des identificateurs d’entrée à long terme. 
    
- Vérifiez que chaque destinataire dans le paramètre _lpRecipList_ possède les propriétés répertoriées dans le paramètre _lpSPropTagArray_ et que ces propriétés s’affichent au début de la liste des destinataires. 
    
MAPI convertit les identificateurs d’entrée de chaque destinataire à court terme des identificateurs d’entrée à long terme. Si nécessaire, les identificateurs d’entrée à long terme des destinataires sont récupérées à partir du fournisseur de carnet d’adresse appropriée et des propriétés supplémentaires sont demandées.
  
Dans une entrée individuelle de destinataire, les propriétés demandées sont triées tout d’abord, suivie de toutes les propriétés qui étaient déjà présentes pour l’entrée. Si une ou plusieurs des propriétés demandées dans le paramètre _lpSPropTagArray_ ne sont pas gérés par le fournisseur de carnet d’adresse appropriée, leurs types de propriétés définira PT_ERROR. Les valeurs de propriété seront fixés à MAPI_E_NOT_FOUND ou une autre valeur qui fournit la raison plus spécifique pourquoi les propriétés ne sont pas disponibles. Chaque structure [SPropValue](spropvalue.md) inclus dans le paramètre _lpRecipList_ doit être alloué séparément en utilisant les fonctions [MAPIAllocateBuffer](mapiallocatebuffer.md) et [MAPIAllocateMore](mapiallocatemore.md) afin qu’elle peut être libérée individuellement. 
  
Pour plus d’informations sur PT_ERROR, reportez-vous à [Types de propriété](property-types.md).
  
## <a name="see-also"></a>Voir aussi



[ADRLIST](adrlist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMessage::ModifyRecipients](imessage-modifyrecipients.md)
  
[Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md)
  
[SPropValue](spropvalue.md)
  
[SRowSet](srowset.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

