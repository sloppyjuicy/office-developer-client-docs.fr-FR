---
title: Propriété canonique PidTagAttachExtension
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachExtension
api_type:
- HeaderDef
ms.assetid: 667da30b-e11c-4040-aecf-bb35eed23722
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 26efa868de29bc8a6a180b717230951b76da26a3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388425"
---
# <a name="pidtagattachextension-canonical-property"></a>Propriété canonique PidTagAttachExtension

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une extension de nom de fichier qui indique le type de document d’une pièce jointe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_EXTENSION, PR_ATTACH_EXTENSION_A, PR_ATTACH_EXTENSION_W  <br/> |
|Identificateur :  <br/> |0x3703  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont définies par l’application cliente au moment de l’envoi. 
  
Le système utilise **PR_ATTACH_EXTENSION** de messagerie lors de la conversion des pièces jointes des messages (conversion dans itinéraire) ou lancer des applications basées sur les pièces jointes dans les messages reçus. Si le client d’envoi ne fournit pas une valeur pour ces propriétés, la banque de messages gère la pièce jointe n’est pas obligée de générer. Le client destinataire doit d’abord vérifier **PR_ATTACH_EXTENSION**et si elle n’est pas fourni, doit analyser l’extension de nom de fichier à partir de la pièce jointe **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) ou **PR_ATTACH_LONG_FILENAME **Propriété ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
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

