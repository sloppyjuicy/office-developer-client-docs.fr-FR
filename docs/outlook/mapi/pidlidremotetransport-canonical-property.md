---
title: PidLidRemoteTransport, propriété canonique
description: Décrit la propriété canonique PidLidRemoteTransport, qui identifie le compte auquel l’élément d’en-tête est associé.
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
ms.openlocfilehash: 92a554036d7498b3475e80f1481922c6d1f272bb
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817640"
---
# <a name="pidlidremotetransport-canonical-property"></a>PidLidRemoteTransport, propriété canonique

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Identifie le compte auquel l’élément d’en-tête est associé, principalement pour implémenter la fonctionnalité Pop Leave on Server. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées  <br/> |dispidRemoteXP  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Remote  <br/> |
|ID long (LID) :  <br/> |0x00008F03  <br/> |
|Type de données :  <br/> |PT_STRING8  <br/> |
|Domaine :  <br/> |Message distant  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété s’applique uniquement aux messages qui ont une classe de message IPM. Distance. Microsoft Outlook conserve un mappage de différents comptes qui sont téléchargés vers un magasin donné dans un message d’informations associées au dossier (FAI), mais il peut également conserver ces informations dans le Registre.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]] 
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

