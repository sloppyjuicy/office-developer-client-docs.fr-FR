---
title: MONTH Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
ms.localizationpriority: medium
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Renvoie un integer de 1 à 12 qui représente un mois.
ms.openlocfilehash: 58fef049190190fc53e1f80c91b5ec05f0b9db59
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770463"
---
# <a name="month-function-visioshapesheet"></a>MONTH Function (VisioShapeSheet)

Renvoie un integer de 1 à 12 qui représente un mois.
  
## <a name="syntax"></a>Syntaxe

MONTH( » ** *datetime* ** « | ** *expression* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Requis  <br/> |**String** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure. |
| _expression_ <br/> |Requis  <br/> |**String** <br/> | Toute expression qui génère une date et une heure. |
| _lcid_ <br/> |Facultatif  <br/> |**Number** <br/> |Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système. |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Le composant d’heure _de date/__heure ou d’expression_ est ignoré. 
  
Aucun arrondissement n’est effectué. Si la chaîne d’entrée est introuvable ou ne peut pas être convertie en un résultat valide, la fonction MONTH renvoie une erreur.
  
La valeur renvoyée est formatée selon le format de date abrégée défini dans les paramètres régionaux actuels de votre système d’exploitation.
  
La fonction MONTH accepte également une valeur de nombre unique pour  _l’expression_ où la partie nombre inte du résultat représente le nombre de jours depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

MONTH("30 mai 1999 13:45:24")
  
Renvoie 5.
  
## <a name="example-2"></a>Exemple 2

MONTH(VALEURDATE("30 mai 1999") + 7 je.)
  
Renvoie 6.
  
## <a name="example-3"></a>Exemple 3

MONTH(35580.6337)
  
Renvoie 5.
  

