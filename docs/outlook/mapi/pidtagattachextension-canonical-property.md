---
title: Propriété canonique PidTagAttachExtension
description: Décrit la propriété canonique PidTagAttachExtension, qui contient une extension de nom de fichier qui indique le type de document d’une pièce jointe.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachExtension
api_type:
- HeaderDef
ms.assetid: 667da30b-e11c-4040-aecf-bb35eed23722
ms.openlocfilehash: 51ad7a02d1e1b44f18e45e8e57b8be2de09ae906
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65811903"
---
# <a name="pidtagattachextension-canonical-property"></a>Propriété canonique PidTagAttachExtension

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une extension de nom de fichier qui indique le type de document d’une pièce jointe. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W  <br/> |
|Identificateur :  <br/> |0x3703  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont définies par l’application cliente au moment de la soumission. 
  
Le système de messagerie utilise **PR_ATTACH_EXTENSION** lors de la conversion de pièces jointes de message (conversion en route) ou du lancement d’applications en fonction des pièces jointes dans les messages reçus. Si le client d’envoi ne fournit pas de valeur pour ces propriétés, le magasin de messages qui gère la pièce jointe n’est pas obligé de la générer. Le client de réception doit d’abord rechercher **PR_ATTACH_EXTENSION** et, s’il n’est pas fourni, analyser l’extension de nom de fichier à partir de la propriété **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) ou **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) de la pièce jointe. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
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

