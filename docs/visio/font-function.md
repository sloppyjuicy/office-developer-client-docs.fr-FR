---
title: Fonction FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Renvoie la valeur de type integer de l’identificateur unique d’une police, spécifié par son nom.
ms.openlocfilehash: afd09ef812b95998a15080c4bb0693ec8d6d10ba
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62782254"
---
# <a name="font-function"></a>Fonction FONT

Renvoie la valeur de type integer de l’identificateur unique d’une police, spécifié par son nom.
  
> [!NOTE]
> Dans la plupart des cas, l’identificateur de police est propre au système. Bien que la police reste établie une fois utilisée dans un fichier, la **fonction FONT** fournit un accès cohérent à une police particulière entre les systèmes et les versions de Visio. Il est recommandé d’utiliser la **fonction FONT** pour affecter des polices au lieu de faire référence directement aux identificateurs de police. 
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013
 
  
## <a name="syntax"></a>Syntaxe

 **FONT**( _« font_name_string »_)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |Requis  <br/> |**chaîne** <br/> |Nom de la police. |
   
## <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Si la chaîne fournie  *pour font_name_string ne*  correspond pas à une police connue, cette fonction renvoie une #VALUE! erreur. 
  
## <a name="example"></a>Exemple

 `FONT("Calibri")`
  
Renvoie la valeur de type integer (4) qui représente l’ID unique de la police « Calibri ».
  

