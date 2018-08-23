---
title: Propriété canonique PidTagAttachPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPathname
api_type:
- HeaderDef
ms.assetid: e19c7cd1-7c56-4f63-8736-d6971c7c5f4d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: add85bbf9c7608434be045bc30a11b8a28ccaa1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578408"
---
# <a name="pidtagattachpathname-canonical-property"></a>Propriété canonique PidTagAttachPathname

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient le chemin d’accès complet et le nom d’une pièce jointe.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W  <br/> |
|Identificateur :  <br/> |0x3708  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les pièces jointes sous-objets exposent ces propriétés. Leur définition indique que les données de pièce jointe n’est pas incluses dans le message, mais ne sont disponibles sur un serveur de fichiers communs. Ces propriétés sont requises en association avec un des indicateurs **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) qui indiquent les pièces jointes par référence : **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**ou **ATTACH_BY_REF_ UNIQUEMENT**. 
  
Chaque répertoire ou un nom de fichier est limité à un nom de huit caractères, plus une extension de trois caractères. Le chemin d’accès globale est limité à 256 caractères. Pour une plate-forme qui prend en charge les noms de fichiers longs, définir ces propriétés et les **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)). 
  
Applications clientes doivent utiliser une convention de dénomination universelle (UNC) dans la plupart des cas, lorsque le fichier est partagé et doit utiliser un chemin absolu lorsque le fichier est local.
  
MAPI ne fonctionne qu’avec les chemins d’accès et le jeu de caractères ANSI, les noms de fichiers. Les clients qui utilisent des chemins d’accès et les noms de fichiers dans un jeu de caractères OEM doivent les convertir au format ANSI avant l’appel de MAPI. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Spécifie les propriétés des messages codés géré par des droits.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[ScLocalPathFromUNC](sclocalpathfromunc.md)
  
[ScUNCFromLocalPath](scuncfromlocalpath.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

