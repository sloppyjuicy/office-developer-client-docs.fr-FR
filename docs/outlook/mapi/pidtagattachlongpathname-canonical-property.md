---
title: Propriété canonique PidTagAttachLongPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongPathname
api_type:
- HeaderDef
ms.assetid: 3262cf95-48b5-4764-a96e-d752ce35b2dc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d8fe8525cf4fc11ac17ed6d73fb5d97e4f2d003e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339367"
---
# <a name="pidtagattachlongpathname-canonical-property"></a>Propriété canonique PidTagAttachLongPathname

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le chemin d'accès long et le nom de fichier complets d'une pièce jointe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W  <br/> |
|Identificateur :  <br/> |0x370D  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés s'appliquent lorsque vous utilisez l'une des valeurs de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) qui indiquent Attachment by reference: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**ou **ATTACH_BY _REF_ONLY**. Les plateformes qui prennent en charge les noms de fichier longs doivent définir à la fois les propriétés **PR_ATTACH_LONG_PATHNAME** ou les propriétés associées et **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) lors de l'envoi, et vérifier **PR_ATTACH_LONG_PATHNAME **ou les propriétés associées en premier lieu lors de la réception. 
  
L'application cliente doit définir ces propriétés sur un chemin d'accès long suggéré et un nom de fichier à utiliser si l'ordinateur hôte qui reçoit un message prend en charge les noms de fichier longs. La définition de ces propriétés indique que les données de pièce jointe ne sont pas incluses dans le message, mais qu'elles sont disponibles sur un serveur de fichiers commun. 
  
Contrairement aux répertoires et aux noms de fichier fournis par **PR_ATTACH_PATHNAME**, ces répertoires et noms de fichier ne sont pas limités à un répertoire à huit caractères ou un nom de fichier et une extension de trois caractères. Au lieu de cela, chaque répertoire ou nom de fichier peut contenir jusqu'à 256 caractères, y compris le nom, l'extension et la période de séparation. Toutefois, le chemin d'accès global est limité à 256 caractères. 
  
Les clients doivent utiliser une convention d'affectation de noms universelle (UNC) dans la plupart des cas lorsque le fichier est partagé, et doivent utiliser un chemin d'accès absolu lorsque le fichier est local.
  
MAPI fonctionne uniquement avec les chemins d'accès et les noms de fichier dans le jeu de caractères ANSI. Les applications clientes qui utilisent des chemins d'accès et des noms de fichiers dans un jeu de caractères OEM doivent les convertir en ANSI avant d'appeler MAPI. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Spécifie les propriétés des messages codés gérés par des droits.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

