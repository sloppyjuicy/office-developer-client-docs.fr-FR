---
title: Propriété canonique PidLidPropertyDefinitionStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPropertyDefinitionStream
api_type:
- COM
ms.assetid: ead35049-e60e-4b46-bf12-f73d77cd36b2
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f7f764d95c2fc36ba6af617333cb47d266cd2aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785338"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a>Propriété canonique PidLidPropertyDefinitionStream

  
  
**S’applique à**: Outlook 
  
Représente les définitions des champs définis par l’utilisateur et les paramètres de liaison de données de champs intégrés d’un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidPropDefStream  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID de type long (capot) :  <br/> |0x00008540  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Configuration d’exécution  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de la propriété **PidLidPropertyDefinitionStream** est enregistrée dans le cadre de la définition de formulaire personnalisé pour le message. 
  
La valeur de cette propriété est un objet stream binaire. Pour plus d’informations sur la structure de ce flux de données, voir [La définition PropertyDefinition flux Structure](propertydefinition-stream-structure.md). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Les champs et les éléments outlook](outlook-items-and-fields.md)
  
[Ajoutez une définition pour un nouveau champ défini par l’utilisateur](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemple de flux de la définition PropertyDefinition](propertydefinition-stream-sample.md)
  
[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

