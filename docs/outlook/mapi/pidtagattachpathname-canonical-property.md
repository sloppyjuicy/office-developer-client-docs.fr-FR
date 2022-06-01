---
title: Propriété canonique PidTagAttachPathname
description: Décrit la propriété canonique PidTagAttachPathname, qui contient le chemin complet et le nom de fichier d’une pièce jointe.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachPathname
api_type:
- HeaderDef
ms.assetid: e19c7cd1-7c56-4f63-8736-d6971c7c5f4d
ms.openlocfilehash: 2c8b50b1b5b63474875c192f8a0b95d73da34563
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812480"
---
# <a name="pidtagattachpathname-canonical-property"></a>Propriété canonique PidTagAttachPathname

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le chemin complet et le nom de fichier d’une pièce jointe.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W  <br/> |
|Identificateur :  <br/> |0x3708  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les sous-objets de pièce jointe exposent ces propriétés. Leur définition indique que les données de pièce jointe ne sont pas incluses dans le message, mais qu’elles sont disponibles sur un serveur de fichiers commun. Ces propriétés sont requises conjointement avec l’un des indicateurs **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) qui indiquent la pièce jointe par référence : **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE** ou **ATTACH_BY_REF_ONLY**. 
  
Chaque répertoire ou nom de fichier est limité à un nom de huit caractères et à une extension à trois caractères. Le chemin d’accès global est limité à 256 caractères. Pour une plateforme qui prend en charge les noms de fichiers longs, définissez ces propriétés et **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)). 
  
Les applications clientes doivent utiliser une convention d’affectation de noms universelle (UNC) dans la plupart des cas lorsque le fichier est partagé, et doivent utiliser un chemin absolu lorsque le fichier est local.
  
MAPI fonctionne uniquement avec les chemins d’accès et les noms de fichiers dans le jeu de caractères ANSI. Les clients qui utilisent des chemins d’accès et des noms de fichiers dans un jeu de caractères OEM doivent les convertir en ANSI avant d’appeler MAPI. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Spécifie les propriétés des messages encodés gérés par des droits.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[ScLocalPathFromUNC](sclocalpathfromunc.md)
  
[ScUNCFromLocalPath](scuncfromlocalpath.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

