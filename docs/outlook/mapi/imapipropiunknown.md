---
title: IMAPIProp IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 02d2b136ed1437ba53ce1e54a202d70a48b2abe9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783919"
---
# <a name="imapiprop--iunknown"></a>IMAPIProp : IUnknown

  
  
**S’applique à**: Outlook 
  
Permet de clients, fournisseurs de services et MAPI travailler avec les propriétés. Tous les objets qui prennent en charge les propriétés implémentent cette interface.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Exposés par :  <br/> |Aucun objet n’expose cette interface directement.  <br/> |
|Implémentée par :  <br/> |Fournisseurs de services et MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes et fournisseurs de services MAPI  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIProp  <br/> |
|Type de pointeur :  <br/> |LPMAPIPROP  <br/> |
|Modèle de transaction :  <br/> |Classe abstraite, jamais implémentée  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetLastError](imapiprop-getlasterror.md) <br/> |Retourne une structure [MAPIERROR](mapierror.md) qui contient des informations sur l’erreur précédente.  <br/> |
|[SaveChanges](imapiprop-savechanges.md) <br/> |Rend permanentes toutes les modifications qui ont été apportées à un objet depuis la dernière opération d’enregistrement.  <br/> |
|[GetProps](imapiprop-getprops.md) <br/> |Récupère la valeur de propriété d’une ou plusieurs propriétés d’un objet.  <br/> |
|[GetPropList](imapiprop-getproplist.md) <br/> |Renvoie les balises de propriété pour toutes les propriétés.  <br/> |
|[OpenProperty](imapiprop-openproperty.md) <br/> |Retourne un pointeur vers une interface qui peut être utilisée pour accéder à une propriété.  <br/> |
|[SetProps](imapiprop-setprops.md) <br/> |Met à jour une ou plusieurs propriétés.  <br/> |
|[DeleteProps](imapiprop-deleteprops.md) <br/> |Supprime une ou plusieurs propriétés d’un objet.  <br/> |
|[CopyTo](imapiprop-copyto.md) <br/> |Copie ou déplace toutes les propriétés, à l’exception de spécifiquement des propriétés exclues.  <br/> |
|[CopyProps](imapiprop-copyprops.md) <br/> |Copie ou déplace des propriétés sélectionnées.  <br/> |
|[GetNamesFromIDs](imapiprop-getnamesfromids.md) <br/> |Fournit les noms des propriétés qui correspondent à un ou plusieurs identificateurs de propriété.  <br/> |
|[GetIDsFromNames](imapiprop-getidsfromnames.md) <br/> |Fournit les identificateurs de propriété qui correspondent à un ou plusieurs noms de propriété.  <br/> |
   
## <a name="remarks"></a>Remarques

 **IMAPIProp** est l’interface de base pour les interfaces suivantes : 
  
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

