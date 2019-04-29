---
title: BOUNDINGBOXRECT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Renvoie les coordonnées du bord spécifié du cadre englobant de la forme.
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418070"
---
# <a name="boundingboxrect-function"></a>Fonction BOUNDINGBOXRECT

Renvoie les coordonnées du bord spécifié du cadre englobant de la forme.
  
## <a name="version-information"></a>Informations de version

Version ajoutée : Visio 2010
 
  
## <a name="syntax"></a>Syntaxe

BOUNDINGBOXRECT (* * *index* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _Index_ <br/> |Obligatoire  <br/> |**Entier** <br/> |Bord du cadre englobant de la forme pour lequel récupérer les coordonnées. Voir la section Remarques pour les valeurs possibles.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

 **Number**
  
## <a name="remarks"></a>Remarques

 *Index* peut prendre l'une des valeurs suivantes. 
  
|**Élément**|**Valeur**|
|:-----|:-----|
|Bord gauche  <br/> |0  <br/> |
|Bord droit  <br/> |0,1  <br/> |
|Bord supérieur  <br/> |n°2  <br/> |
|Bord inférieur  <br/> |3  <br/> |
   
Si la forme a un parent, la valeur renvoyée se trouve dans le système de coordonnées de ce parent.
  

