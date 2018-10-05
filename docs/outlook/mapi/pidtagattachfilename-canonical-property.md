---
title: Propriété canonique PidTagAttachFilename
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFilename
api_type:
- HeaderDef
ms.assetid: cbf34dd6-7733-47f6-9c41-9d82656ca9dc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f5dcf90e8224f1bf2e96042a7344109293cc2c3f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385708"
---
# <a name="pidtagattachfilename-canonical-property"></a>Propriété canonique PidTagAttachFilename

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom de fichier de base et l’extension à l’exclusion du chemin d’accès d’une pièce jointe.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W  <br/> |
|Identificateur :  <br/> |0x3704  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les objets attachment exposent ces propriétés qui s’appliquent aux valeurs de la **PR_ATTACH_METHOD** **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**et **ATTACH_BY_REF_ONLY** Propriété ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)). **PR_ATTACH_FILENAME** et propriétés associées sont requis quand un de ces valeurs est utilisé. 
  
Ces propriétés peuvent être utilisées comme nom de fichier suggéré pour enregistrer la pièce jointe et leur fournir l’extension de nom de fichier si la propriété **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) n’est pas fournie. 
  
Le nom de fichier est limité à huit caractères et une extension de trois caractères. Pour une plate-forme qui prend en charge les noms de fichiers longs, définissez cette propriété et la propriété **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)). 
  
MAPI ne fonctionne qu’avec les noms de fichiers et autres chaînes passé, dans le jeu de caractères National Institute ANSI (American Standards). Les applications clientes qui utilisent des noms de fichiers dans un jeu de caractères OEM (OEM) doivent les convertir au format ANSI avant l’appel de MAPI. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Spécifie les propriétés des messages codés géré par des droits.
    
[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)
  
> Spécifie S/MIME signés et chiffrés des propriétés de message.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode des objets message et la pièce jointe à une représentation sous forme de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

