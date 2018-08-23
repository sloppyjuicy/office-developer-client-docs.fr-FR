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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c0a3a96c3d8835550c4b0fda233183214cb4a786
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587424"
---
# <a name="pidtagattachlongpathname-canonical-property"></a>Propriété canonique PidTagAttachLongPathname

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient le long de chemin d’accès complet et le nom d’une pièce jointe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W  <br/> |
|Identificateur :  <br/> |0x370D  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés sont applicables lorsque vous utilisez une des valeurs de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) qui indiquent les pièces jointes par référence : **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**ou **ATTACH_BY _REF_ONLY**. Plateformes qui prennent en charge les noms de fichiers longs doivent définir les propriétés de **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) lors de l’envoi et doit vérifier **PR_ATTACH_LONG_PATHNAME et de propriétés associées ou les **PR_ATTACH_LONG_PATHNAME** **ou des propriétés associées tout d’abord lors de la réception. 
  
L’application cliente doit définir ces propriétés pour un chemin d’accès long suggérée et un nom à utiliser si l’ordinateur hôte reçoit un message prend en charge les noms de fichiers longs. Définition de ces propriétés indique que les données de pièce jointe n’est pas incluses dans le message, mais ne sont disponibles sur un serveur de fichiers communs. 
  
Contrairement aux répertoires et noms de fichiers fournis par **PR_ATTACH_PATHNAME**, ces répertoires et les noms de fichiers ne sont pas restreints vers un répertoire de huit caractères ou de nom de fichier plus extension de trois caractères. Au lieu de cela, chaque répertoire ou un nom de fichier peut être jusqu'à 256 caractères long, y compris le nom, extension et une période séparateur. Toutefois, le chemin d’accès globale est limité à 256 caractères. 
  
Clients doivent utiliser une convention de dénomination universelle (UNC) dans la plupart des cas, lorsque le fichier est partagé et doit utiliser un chemin absolu lorsque le fichier est local.
  
MAPI ne fonctionne qu’avec les chemins d’accès et le jeu de caractères ANSI, les noms de fichiers. Les applications clientes qui utilisent des chemins d’accès et les noms de fichiers dans un jeu de caractères OEM doivent les convertir au format ANSI avant l’appel de MAPI. 
  
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



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

