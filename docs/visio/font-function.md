---
title: Fonction de la police
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Renvoie la valeur d’entier de l’identificateur unique pour une police, spécifiée par nom.
ms.openlocfilehash: 4afd2aa05f2103675bf0df8db5cc7ea21f45fe71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788673"
---
# <a name="font-function"></a>Fonction de la police

Renvoie la valeur d’entier de l’identificateur unique pour une police, spécifiée par nom.
  
> [!NOTE]
> Dans la plupart des cas, l’identificateur de la police est spécifiques au système. Bien que la police reste établie autrefois utilisé dans un fichier, la fonction de **police** offre un accès cohérent à une police spécifique sur les systèmes et les versions de Visio. Il est recommandé d’utiliser la fonction de la **police** pour affecter des polices au lieu de faire référence aux identificateurs de police directement. 
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013 
  
## <a name="syntax"></a>Syntaxe

 **Police** ( _« font_name_string »_)
  
### <a name="parameters"></a>Paramètres

|**Name**|**Obligatoire/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |Obligatoire  <br/> |**string** <br/> |Nom de la police.  <br/> |
   
## <a name="return-value"></a>Valeur renvoy�e

Entier
  
## <a name="remarks"></a>Remarques

Si la chaîne fournie pour *font_name_string* ne correspond pas à une police connue, cette fonction renvoie une #VALUE ! erreur. 
  
## <a name="example"></a>Exemple

 `FONT("Calibri")`
  
Renvoie la valeur d’entier (4) qui représente l’identificateur unique pour la police « Calibri ».
  

