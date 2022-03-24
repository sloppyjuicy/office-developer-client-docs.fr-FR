---
title: Propriété canonique PidTagDelegateFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDelegateFlags
api_type:
- HeaderDef
ms.assetid: 3a504594-204c-472c-8be7-dca154c94ea2
description: Spécifie si un délégué peut afficher les objets de message privés du délégant. Cette propriété doit être définie dans l’objet d’informations du délégué.
ms.openlocfilehash: 0de4d8459a7a1f48723e7e0ba6da1b076ce4bb38
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63762416"
---
# <a name="pidtagdelegateflags-canonical-property"></a>Propriété canonique PidTagDelegateFlags

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie si un délégué peut afficher les objets de message privés du délégant.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_DELEGATE_FLAGS  <br/> |
|Identificateur :  <br/> |0x686B  <br/> |
|Type de données :  <br/> |PT_MV_LONG  <br/> |
|Domaine :  <br/> |Message défini comme transmettable par la classe  <br/> |
   
## <a name="remarks"></a>Remarques

Chaque entrée de cette propriété doit être définie sur l’une des valeurs suivantes.
  
|**Indicateur**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|HidePrivate  <br/> |0  <br/> |Le délégué ne doit pas être autorisé à afficher les objets de message privés. |
|ShowPrivate  <br/> |1  <br/> |Le délégué doit être autorisé à afficher les objets de message privés. |
   
Cette propriété doit être définie dans l’objet d’informations du délégué. La valeur de « ShowPrivate » indique que le délégant souhaite rendre les objets de message privés visibles. Cette préférence s’applique à tous les dossiers pour lesquels le délégué a un rôle de réviseur, d’auteur ou d’éditeur.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Spécifie les méthodes de connexion et de configuration des boîtes aux lettres en tant que délégués, ainsi que les interactions avec les objets de message et de calendrier lorsqu’ils agissent pour le compte d’un autre utilisateur.
    
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

