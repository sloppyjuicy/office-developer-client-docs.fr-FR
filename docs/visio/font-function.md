---
title: Fonction FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Renvoie la valeur entière de l'identificateur unique d'une police, spécifiée par son nom.
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422172"
---
# <a name="font-function"></a>Fonction FONT

Renvoie la valeur entière de l'identificateur unique d'une police, spécifiée par son nom.
  
> [!NOTE]
> Dans la plupart des cas, l'identificateur de police est propre au système. Bien que la police reste créée une fois utilisée dans un fichier, la fonction **font** offre un accès cohérent à une police particulière entre les systèmes et les versions de Visio. Il est recommandé d'utiliser la fonction **font** pour affecter des polices au lieu de faire référence à des identificateurs de police directement. 
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2013
 
  
## <a name="syntax"></a>Syntaxe

 **Police** ( _«font_name_string»_)
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _font_name_string_ <br/> |Obligatoire  <br/> |**chaîne** <br/> |Nom de la police.  <br/> |
   
## <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Si la chaîne fournie pour *font_name_string* ne correspond pas à une police connue, cette fonction renvoie une #VALUE! «. 
  
## <a name="example"></a>Exemple

 `FONT("Calibri")`
  
Renvoie la valeur de type Integer (4) représentant l'ID unique de la police «Calibri».
  

