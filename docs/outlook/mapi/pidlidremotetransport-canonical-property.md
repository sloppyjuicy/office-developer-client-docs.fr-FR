---
title: Propri t canonique PidLidRemoteTransport
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidRemoteTransport
api_type:
- COM
ms.assetid: b3b30d6a-05cd-4dd1-a162-20768f12e680
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d40ec12e3bf171bf85fd0c59708e1a4bb7324b9d
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63721928"
---
# <a name="pidlidremotetransport-canonical-property"></a>Propri t canonique PidLidRemoteTransport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Identifie le compte à quel compte l’élément d’en-tête est associé, principalement pour implémenter la fonctionnalité POP Leave on Server. 
  
|Propriété |Valeur |
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

