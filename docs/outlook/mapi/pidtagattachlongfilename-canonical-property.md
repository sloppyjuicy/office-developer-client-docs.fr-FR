---
title: PidTagAttachLongFilename, propriété canonique
description: Décrit la propriété canonique PidTagAttachLongFilename, qui contient le nom de fichier long et l’extension d’une pièce jointe, à l’exclusion du chemin d’accès.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachLongFilename
api_type:
- HeaderDef
ms.assetid: 83b69e8f-0b5a-4992-b5b8-160d3bdfa22a
ms.openlocfilehash: d31fea1f47b72c070be02fdaf418ce23884c1ece
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815603"
---
# <a name="pidtagattachlongfilename-canonical-property"></a>PidTagAttachLongFilename, propriété canonique

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le nom de fichier long et l’extension d’une pièce jointe, à l’exclusion du chemin d’accès. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W  <br/> |
|Identificateur :  <br/> |0x3707  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés se rapportent aux valeurs ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE et ATTACH_BY_REF_ONLY de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)). Les plateformes qui prennent en charge les noms de fichiers longs doivent définir les propriétés **PR_ATTACH_LONG_FILENAME** et **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) lors de l’envoi et doivent vérifier **PR_ATTACH_LONG_FILENAME** d’abord lors de la réception. 
  
L’application cliente doit définir cette propriété sur un nom de fichier long suggéré à utiliser si l’ordinateur hôte qui reçoit un message prend en charge les noms de fichiers longs. **PR_ATTACH_LONG_FILENAME** peut être utilisé comme nom de fichier pour enregistrer la pièce jointe et pour fournir l’extension de nom de fichier si la propriété **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) n’est pas fournie. 
  
Contrairement au nom de fichier fourni par **PR_ATTACH_FILENAME**, ce nom n’est pas limité à un nom de fichier à huit caractères et à une extension à trois caractères. Au lieu de cela, il peut avoir jusqu’à 256 caractères, y compris le nom de fichier, l’extension et la période de séparateur. 
  
MAPI fonctionne uniquement avec les noms de fichiers dans le jeu de caractères ANSI. Les applications clientes qui utilisent des noms de fichiers dans un jeu de caractères OEM doivent les convertir en ANSI avant d’appeler MAPI. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions e-mail standard Internet en objets de message.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Spécifie les propriétés des messages encodés gérés par des droits.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour représenter les messages vocaux et de télécopie.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mmapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

