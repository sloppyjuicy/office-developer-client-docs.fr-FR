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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357784"
---
# <a name="pidlidflagstring-canonical-property"></a>Propriété canonique PidLidFlagString

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un index qui identifie l’un des ensembles de chaînes de texte prédéfinës associées à l’indicateur.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidFlagStringEnum  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x000085C0  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Tâche  <br/> |
   
## <a name="remarks"></a>Remarques

Si cette propriété est définie, les clients doivent utiliser la valeur de chaîne correspondante dans les tableaux ci-dessous (par exemple, pour remplacer une chaîne traduite dans la langue de l’utilisateur actuel) et doivent ignorer la valeur définie dans **dispidFlagRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) et **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)). 
  
Les valeurs par défaut suggérées à l’utilisateur pour les objets contact sont les suivantes :
  
|**Valeur**|**Chaîne anglaise**|
|:-----|:-----|
|0x00000000 ou non présent  <br/> | Suivez les instructions relatives à l’affichage **de dispidFlagRequest**.  <br/> |
|0x0000006E  <br/> |« Suivi »  <br/> |
|0x0000006F  <br/> |« Appeler »  <br/> |
|0x00000070  <br/> |« Organiser une réunion »  <br/> |
|0x00000071  <br/> |« Envoyer un e-mail »  <br/> |
|0x00000072  <br/> |« Envoyer une lettre »  <br/> |
   
Les valeurs par défaut suggérées à l’utilisateur pour tous les autres objets de message sont les suivantes :
  
|**Valeur**|**Chaîne anglaise**|
|:-----|:-----|
|0x00000000 ou non présent  <br/> | Suivez les instructions relatives à l’affichage **de dispidFlagRequest**.  <br/> |
|0x00000001  <br/> |« Appeler »  <br/> |
|0x00000002  <br/> |« Ne pas avancer »  <br/> |
|0x00000003  <br/> |« Suivi »  <br/> |
|0x00000004  <br/> |« Pour vos informations »  <br/> |
|0x00000005  <br/> |« Transférer »  <br/> |
|0x00000006  <br/> |« Aucune réponse nécessaire »  <br/> |
|0x00000007  <br/> |« Lecture »  <br/> |
|0x00000008  <br/> |« Répondre »  <br/> |
|0x00000009  <br/> |« Répondre à tous »  <br/> |
|0x0000000A  <br/> |« Révision »  <br/> |
   
Toutes les chaînes spécifiées ci-dessus peuvent être traduites dans la langue de l’utilisateur, le cas échéant.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations liées au marquage.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

