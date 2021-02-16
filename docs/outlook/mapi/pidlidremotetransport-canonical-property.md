---
title: Propri t canonique PidLidRemoteTransport
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
# <a name="pidlidremotetransport-canonical-property"></a>Propri t canonique PidLidRemoteTransport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Identifie le compte à quel compte l’élément d’en-tête est associé, principalement pour implémenter la fonctionnalité POP Leave on Server. 
  
|||
|:-----|:-----|
|Propriétés associées  <br/> |dispidRemoteXP  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Remote  <br/> |
|ID long (LID) :  <br/> |0x00008F03  <br/> |
|Type de données :  <br/> |PT_STRING8  <br/> |
|Domaine :  <br/> |Message distant  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété n’est pertinente que pour les messages qui ont une classe de message IPM. Distant. Microsoft Outlook conserve un mappage de différents comptes qui sont téléchargés vers une banque donnée dans un message FAI (Folder Associated Information), mais il peut également conserver ces informations dans le Registre.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]] 
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

