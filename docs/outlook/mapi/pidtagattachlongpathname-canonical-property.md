---
title: Propriété canonique PidTagAttachLongPathname
description: Décrit la propriété canonique PidTagAttachLongPathname, qui contient le chemin long complet et le nom de fichier d’une pièce jointe.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachLongPathname
api_type:
- HeaderDef
ms.assetid: 3262cf95-48b5-4764-a96e-d752ce35b2dc
ms.openlocfilehash: 56e69741d2e32d8aa474e5df061a0abd29470b13
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815309"
---
# <a name="pidtagattachlongpathname-canonical-property"></a>Propriété canonique PidTagAttachLongPathname

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient le chemin long complet et le nom de fichier d’une pièce jointe. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W  <br/> |
|Identificateur :  <br/> |0x370D  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés s’appliquent lorsque vous utilisez l’une des valeurs de la propriété **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) qui indiquent la pièce jointe par référence : **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE** ou **ATTACH_BY_REF_ONLY**. Les plateformes qui prennent en charge les noms de fichiers longs doivent définir **les** propriétés PR_ATTACH_LONG_PATHNAME ou associées et les propriétés **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) lors de l’envoi, et doivent d’abord vérifier **PR_ATTACH_LONG_PATHNAME** ou les propriétés associées lors de la réception. 
  
L’application cliente doit définir ces propriétés sur un chemin long suggéré et un nom de fichier à utiliser si l’ordinateur hôte qui reçoit un message prend en charge les noms de fichiers longs. La définition de ces propriétés indique que les données de pièce jointe ne sont pas incluses dans le message, mais qu’elles sont disponibles sur un serveur de fichiers commun. 
  
Contrairement aux répertoires et noms de fichiers fournis par **PR_ATTACH_PATHNAME**, ces répertoires et noms de fichiers ne sont pas limités à un répertoire de huit caractères ou à un nom de fichier plus une extension à trois caractères. Au lieu de cela, chaque répertoire ou nom de fichier peut avoir jusqu’à 256 caractères, y compris le nom, l’extension et la période de séparateur. Toutefois, le chemin d’accès global est limité à 256 caractères. 
  
Les clients doivent utiliser une convention d’affectation de noms universelle (UNC) dans la plupart des cas lorsque le fichier est partagé, et doivent utiliser un chemin absolu lorsque le fichier est local.
  
MAPI fonctionne uniquement avec les chemins d’accès et les noms de fichiers dans le jeu de caractères ANSI. Les applications clientes qui utilisent des chemins d’accès et des noms de fichiers dans un jeu de caractères OEM doivent les convertir en ANSI avant d’appeler MAPI. 
  
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



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

