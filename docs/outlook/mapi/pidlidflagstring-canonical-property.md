---
title: Propriété canonique PidLidFlagString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagString
api_type:
- COM
ms.assetid: 4cf1e08b-c869-4965-a1e4-512a0684700f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b3cd88db7e93b53990cf0181af623ebca75f0c6e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395580"
---
# <a name="pidlidflagstring-canonical-property"></a>Propriété canonique PidLidFlagString

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un index qui identifie un ensemble prédéfini de chaînes de texte associé à l’indicateur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidFlagStringEnum  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID de type long (capot) :  <br/> |0x000085C0  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est définie, les clients doivent utiliser la valeur de chaîne correspondant dans les tableaux ci-dessous (par exemple, pour remplacer une chaîne qui est convertie en langue de l’utilisateur actuel) et doivent ignorer la valeur définie dans **dispidFlagRequest** ([ PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) et **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)). 
  
Les valeurs par défaut suggérés pour l’utilisateur pour les objets contact sont les suivantes :
  
|**Valeur**|**Chaîne en anglais**|
|:-----|:-----|
|0 x 00000000 ou absent  <br/> | Suivez les instructions relatives à l’affichage de **dispidFlagRequest**.  <br/> |
|0x0000006E  <br/> |« Suivi »  <br/> |
|0x0000006F  <br/> |« Appel »  <br/> |
|0 x 00000070  <br/> |« Organiser la réunion »  <br/> |
|0 x 00000071  <br/> |« Envoyer un courrier électronique »  <br/> |
|0x00000072  <br/> |« Envoyer la lettre »  <br/> |
   
Les valeurs par défaut suggérés pour l’utilisateur pour tous les autres objets de message sont les suivantes :
  
|**Valeur**|**Chaîne en anglais**|
|:-----|:-----|
|0 x 00000000 ou absent  <br/> | Suivez les instructions relatives à l’affichage de **dispidFlagRequest**.  <br/> |
|0x00000001  <br/> |« Appel »  <br/> |
|0x00000002  <br/> |« Ne pas transférer »  <br/> |
|0 x 00000003  <br/> |« Suivi »  <br/> |
|0 x 00000004  <br/> |« Pour votre Information »  <br/> |
|0 x 00000005  <br/> |« Transférer »  <br/> |
|0 x 00000006  <br/> |« Aucune réponse nécessaire »  <br/> |
|0 x 00000007  <br/> |« Lecture »  <br/> |
|0 x 00000008  <br/> |« Reply »  <br/> |
|0 x 00000009  <br/> |« Répondre à tous »  <br/> |
|0x0000000A  <br/> |« Révision »  <br/> |
   
Toutes les chaînes spécifiés ci-dessus peuvent être traduits à la langue de l’utilisateur, le cas échéant.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées aux marquage.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

