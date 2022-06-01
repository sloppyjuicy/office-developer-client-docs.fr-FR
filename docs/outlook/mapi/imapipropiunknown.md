---
title: IMAPIProp IUnknown
description: IMAPIPropIUnknown permet aux clients, aux fournisseurs de services et à MAPI d’utiliser des propriétés. Tous les objets qui prennent en charge les propriétés implémentent cette interface.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
ms.openlocfilehash: 5bf10d6af964edcf96dc2123c1b98a6757cf8c96
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812089"
---
# <a name="imapiprop--iunknown"></a>IMAPIProp : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux clients, aux fournisseurs de services et à MAPI d’utiliser des propriétés. Tous les objets qui prennent en charge les propriétés implémentent cette interface.
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Aucun objet n’expose directement cette interface. |
|Implémenté par :  <br/> |Fournisseurs de services et MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes, fournisseurs de services et MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIProp  <br/> |
|Type de pointeur :  <br/> |LPMAPIPROP  <br/> |
|Modèle de transaction :  <br/> |Classe abstraite, jamais implémentée  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member|Description|
|:-----|:-----|
|[Getlasterror](imapiprop-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente. |
|[SaveChanges](imapiprop-savechanges.md) <br/> |Rend permanentes les modifications apportées à un objet depuis la dernière opération d’enregistrement. |
|[GetProps](imapiprop-getprops.md) <br/> |Récupère la valeur de propriété d’une ou plusieurs propriétés d’un objet. |
|[GetPropList](imapiprop-getproplist.md) <br/> |Retourne des balises de propriété pour toutes les propriétés. |
|[OpenProperty](imapiprop-openproperty.md) <br/> |Retourne un pointeur vers une interface qui peut être utilisée pour accéder à une propriété. |
|[SetProps](imapiprop-setprops.md) <br/> |Met à jour une ou plusieurs propriétés. |
|[DeleteProps](imapiprop-deleteprops.md) <br/> |Supprime une ou plusieurs propriétés d’un objet. |
|[CopyTo](imapiprop-copyto.md) <br/> |Copie ou déplace toutes les propriétés, à l’exception des propriétés spécifiquement exclues. |
|[CopyProps](imapiprop-copyprops.md) <br/> |Copie ou déplace les propriétés sélectionnées. |
|[GetNamesFromIDs](imapiprop-getnamesfromids.md) <br/> |Fournit les noms de propriétés qui correspondent à un ou plusieurs identificateurs de propriété. |
|[GetIDsFromNames](imapiprop-getidsfromnames.md) <br/> |Fournit les identificateurs de propriété qui correspondent à un ou plusieurs noms de propriétés. |
   
## <a name="remarks"></a>Remarques

 **IMAPIProp** est l’interface de base pour les interfaces suivantes : 
  
- [IAttach](iattachimapiprop.md)
    
- [IMailUser](imailuserimapiprop.md)
    
- [IMAPIContainer](imapicontainerimapiprop.md)
    
- [IMAPIFormInfo](imapiforminfoimapiprop.md)
    
- [IMAPIStatus](imapistatusimapiprop.md)
    
- [Imessage](imessageimapiprop.md)
    
- [IMsgStore](imsgstoreimapiprop.md)
    
- [IProfSect](iprofsectimapiprop.md)
    
- [IPropData](ipropdataimapiprop.md)
    
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

