---
title: Propriété canonique PidLidPropertyDefinitionStream
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2ba6fc19d52e0dbc54c863e0906bf8ff56b512a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616676"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a>Propriété canonique PidLidPropertyDefinitionStream

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Représente les définitions des champs définis par l’utilisateur et les paramètres de liaison de données des champs intégrés d’un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidPropDefStream  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008540  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Configuration au moment de l’exécuter  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de la **propriété PidLidPropertyDefinitionStream** est enregistrée dans le cadre de la définition de formulaire personnalisée du message. 
  
La valeur de cette propriété est un flux binaire. Pour plus d’informations sur la structure de ce flux, voir [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Outlook Éléments et champs](outlook-items-and-fields.md)
  
[Ajouter une définition pour un nouveau champ User-Defined de recherche](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Exemple de flux PropertyDefinition](propertydefinition-stream-sample.md)
  
[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

