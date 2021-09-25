---
title: IMAPIProp IUnknown
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 9f7667f4e1776b8aa5d6a455c847012328a35506
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567577"
---
# <a name="imapiprop--iunknown"></a>IMAPIProp : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet aux clients, aux fournisseurs de services et à MAPI d’fonctionner avec les propriétés. Tous les objets qui la prise en charge des propriétés implémentent cette interface.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposé par :  <br/> |Aucun objet n’expose cette interface directement.  <br/> |
|Implémenté par :  <br/> |Fournisseurs de services et MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes, fournisseurs de services et MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIProp  <br/> |
|Type de pointeur :  <br/> |LPMAPIPROP  <br/> |
|Modèle de transaction :  <br/> |Classe abstraite, jamais implémentée  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetLastError](imapiprop-getlasterror.md) <br/> |Renvoie une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente.  <br/> |
|[SaveChanges](imapiprop-savechanges.md) <br/> |Rend permanentes les modifications apportées à un objet depuis la dernière opération d’enregistrer.  <br/> |
|[GetProps](imapiprop-getprops.md) <br/> |Extrait la valeur de propriété d’une ou plusieurs propriétés d’un objet.  <br/> |
|[GetPropList](imapiprop-getproplist.md) <br/> |Renvoie des balises de propriété pour toutes les propriétés.  <br/> |
|[OpenProperty](imapiprop-openproperty.md) <br/> |Renvoie un pointeur vers une interface qui peut être utilisée pour accéder à une propriété.  <br/> |
|[SetProps](imapiprop-setprops.md) <br/> |Met à jour une ou plusieurs propriétés.  <br/> |
|[DeleteProps](imapiprop-deleteprops.md) <br/> |Supprime une ou plusieurs propriétés d’un objet.  <br/> |
|[CopyTo](imapiprop-copyto.md) <br/> |Copie ou déplace toutes les propriétés, à l’exception des propriétés spécifiquement exclues.  <br/> |
|[CopyProps](imapiprop-copyprops.md) <br/> |Copie ou déplace les propriétés sélectionnées.  <br/> |
|[GetNamesFromIDs](imapiprop-getnamesfromids.md) <br/> |Fournit les noms de propriété qui correspondent à un ou plusieurs identificateurs de propriété.  <br/> |
|[GetIDsFromNames](imapiprop-getidsfromnames.md) <br/> |Fournit les identificateurs de propriété qui correspondent à un ou plusieurs noms de propriété.  <br/> |
   
## <a name="remarks"></a>Remarques

 **IMAPIProp est** l’interface de base pour les interfaces suivantes : 
  
- [IAttach](iattachimapiprop.md)
    
- [IMailUser](imailuserimapiprop.md)
    
- [IMAPIContainer](imapicontainerimapiprop.md)
    
- [IMAPIFormInfo](imapiforminfoimapiprop.md)
    
- [IMAPIStatus](imapistatusimapiprop.md)
    
- [IMessage](imessageimapiprop.md)
    
- [IMsgStore](imsgstoreimapiprop.md)
    
- [IProfSect](iprofsectimapiprop.md)
    
- [IPropData](ipropdataimapiprop.md)
    
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

