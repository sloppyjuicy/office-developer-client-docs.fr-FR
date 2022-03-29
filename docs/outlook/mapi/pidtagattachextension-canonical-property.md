---
title: Propriété canonique PidTagAttachExtension
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2c40bf5492e760a8950e4f8026cdcc8867896e53
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64454466"
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
  
Le système de messagerie **utilise PR_ATTACH_EXTENSION lors** de la conversion de pièces jointes de messages (conversion sur route) ou du lancement d’applications basées sur des pièces jointes dans les messages reçus. Si le client d’envoi ne fournit pas de valeur pour ces propriétés, la boutique de messages qui gère la pièce jointe n’est pas tenue de la générer. Le client de réception doit d’abord vérifier la PR_ATTACH_EXTENSION **et, si** elle n’est pas fournie, doit l’parer à partir de la propriété **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) ou **PR_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) de la pièce jointe. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

