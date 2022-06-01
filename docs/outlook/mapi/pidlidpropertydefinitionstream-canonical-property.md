---
title: Propriété canonique PidLidPropertyDefinitionStream
description: Décrit la propriété canonique PidLidPropertyDefinitionStream, qui est enregistrée dans le cadre de la définition de formulaire personnalisée pour le message.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidPropertyDefinitionStream
api_type:
- COM
ms.assetid: ead35049-e60e-4b46-bf12-f73d77cd36b2
ms.openlocfilehash: 1a50d12b0d455cce2be92c14b4b1be7c2ce2df00
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817661"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a>Propriété canonique PidLidPropertyDefinitionStream

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente les définitions de champs définis par l’utilisateur et les paramètres de liaison de données des champs intégrés d’un message.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidPropDefStream  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008540  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Configuration au moment de l’exécution  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de la propriété **PidLidPropertyDefinitionStream** est enregistrée dans le cadre de la définition de formulaire personnalisée pour le message. 
  
La valeur de cette propriété est un flux binaire. Pour plus d’informations sur la structure de ce flux, consultez [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Outlook éléments et champs](outlook-items-and-fields.md)
  
[Ajouter une définition pour un nouveau champ User-Defined](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition Stream Sample](propertydefinition-stream-sample.md)
  
[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

