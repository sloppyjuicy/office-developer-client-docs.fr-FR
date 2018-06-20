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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b0f86b2260299d2d0294598628f2895c50ed9452
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785393"
---
# <a name="pidlidremotetransport-canonical-property"></a>Propriété canonique PidLidRemoteTransport

  
  
**S’applique à**: Outlook 
  
Identifie le compte de l’élément d’en-tête est associé, principalement pour implémenter le congé POP sur les fonctionnalités du serveur. 
  
|||
|:-----|:-----|
|Propriétés associées  <br/> |dispidRemoteXP  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Remote  <br/> |
|ID de type long (capot) :  <br/> |0x00008F03  <br/> |
|Type de données :  <br/> |PT_STRING8  <br/> |
|Zone :  <br/> |Message à distance  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété s’applique uniquement sur les messages qui ont une classe de message IPM. À distance. Microsoft Outlook gère un mappage des différents comptes téléchargez sur une banque donnée dans un message de dossier associé informations (FAI), mais peut également ces informations dans le Registre.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]] 
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

