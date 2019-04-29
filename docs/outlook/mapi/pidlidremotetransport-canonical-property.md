---
title: Propriété canonique PidLidRemoteTransport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ddedc2ca0785be2fe4850ec3cfdf979d1e5f2798
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439442"
---
# <a name="pidlidremotetransport-canonical-property"></a>Propriété canonique PidLidRemoteTransport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Identifie le compte auquel l'élément d'en-tête est associé, principalement pour implémenter la fonctionnalité laisser le POP sur le serveur. 
  
|||
|:-----|:-----|
|Propriétés associées  <br/> |dispidRemoteXP  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Remote  <br/> |
|ID long (couvercle):  <br/> |0x00008F03  <br/> |
|Type de données :  <br/> |PT_STRING8  <br/> |
|Domaine :  <br/> |Message distant  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété s'applique uniquement aux messages dont la classe de message est IPM. À. Microsoft Outlook conserve un mappage des différents comptes qui sont téléchargés vers un magasin donné dans un message d'informations sur le dossier (FAI), mais il peut également conserver ces informations dans le registre.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]] 
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

