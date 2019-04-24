---
title: HOUR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Renvoie un entier compris entre 0 et 23 représentant l'heure du jour de dateheure ou expression.
ms.openlocfilehash: 1d0c6ec2bd80605401f44d2a5ef6e3d41bc72556
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329966"
---
# <a name="hour-function-visioshapesheet"></a>HOUR Function (VisioShapeSheet)

Renvoie un entier compris entre 0 et 23 représentant l'heure du jour de _DateHeure_ ou _expression_.
  
## <a name="syntax"></a>Syntaxe

HOUR ("* * *DateTime* * *" | * * *expression* * * [, * * *LCID* * *]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _structure_ <br/> |Obligatoire  <br/> |**String** <br/> | Chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Obligatoire  <br/> |**Réelle** <br/> |Expression qui génère une date et une heure.  <br/> |
| _lcid_ <br/> |Facultatif  <br/> |**Number** <br/> | Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
## <a name="remarks"></a>Remarques

Le composant date de *DateTime* et *expression* est ignoré. 
  
Aucun arrondissement n’est effectué. Si le *DateTime* est manquant ou ne peut pas être converti en un résultat valide, la fonction renvoie une erreur. 
  
La valeur renvoyée est formatée selon le format horaire défini dans les paramètres régionaux actuels de votre système d’exploitation. 
  
La fonction HOUR accepte également une valeur numérique simple pour *expression* où la partie décimale du résultat représente la fraction du jour depuis minuit. 
  
## <a name="example-1"></a>Exemple 1

HOUR ("15:45")
  
Renvoie 15.
  
## <a name="example-2"></a>Exemple 2

HOUR("30 mai 1997 15:45:24")
  
Renvoie 15.
  
## <a name="example-3"></a>Exemple 3

HEURE (0.5)
  
Renvoie 12.
  
## <a name="example-4"></a>Exemple 4

HOUR ("5/30/1997")
  
Renvoie 0.
  

