---
title: PidTagAttachFilename, propriété canonique
description: Décrit la propriété canonique PidTagAttachFilename, qui contient le nom et l’extension de fichier de base d’une pièce jointe, à l’exclusion du chemin d’accès.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachFilename
api_type:
- HeaderDef
ms.assetid: cbf34dd6-7733-47f6-9c41-9d82656ca9dc
ms.openlocfilehash: 4bd77d4b0010f9a06cc061a7d9272fdead379769
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817787"
---
# <a name="pidtagattachfilename-canonical-property"></a>PidTagAttachFilename, propriété canonique

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom et l’extension de fichier de base d’une pièce jointe, à l’exclusion du chemin d’accès.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_FILENAME, PR_ATTACH_FILENAME_A, PR_ATTACH_FILENAME_W  <br/> |
|Identificateur :  <br/> |0x3704  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les objets en pièce jointe exposent ces propriétés qui se rapportent aux valeurs **ATTACH_BY_VALUE**, **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE** et **ATTACH_BY_REF_ONLY** de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)). **PR_ATTACH_FILENAME** et les propriétés associées sont requises lorsque l’une de ces valeurs est utilisée. 
  
Ces propriétés peuvent être utilisées comme nom de fichier suggéré pour enregistrer la pièce jointe et fournir l’extension de nom de fichier si la propriété **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) n’est pas fournie. 
  
Le nom de fichier est limité à huit caractères plus une extension à trois caractères. Pour une plateforme qui prend en charge les noms de fichiers longs, définissez cette propriété et la propriété **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)). 
  
MAPI fonctionne uniquement avec les noms de fichiers et d’autres chaînes qui lui sont passées, dans le jeu de caractères ANSI (American National Standards Institute). Les applications clientes qui utilisent des noms de fichiers dans un jeu de caractères OEM (fabricant d’équipement d’origine) doivent les convertir en ANSI avant d’appeler MAPI. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions e-mail standard Internet en objets de message.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Spécifie les propriétés des messages encodés gérés par des droits.
    
[[MS-OXOSMIME]](https://msdn.microsoft.com/library/bb17d126-d211-462c-8cd3-454ed33c8746%28Office.15%29.aspx)
  
> Spécifie les propriétés des messages signés et chiffrés S/MIME.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Encode et décode les objets de message et de pièce jointe dans une représentation de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

