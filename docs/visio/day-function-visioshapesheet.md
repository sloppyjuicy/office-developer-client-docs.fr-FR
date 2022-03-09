---
title: DAY Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
ms.localizationpriority: medium
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: Renvoie un integer, de 1 à 31, qui représente le jour dans l’expression ou l’heure de date. La fonction DAY utilise le calendrier grégorien.
ms.openlocfilehash: 5334e8c4f94e3d385932ed9440391242db086271
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379856"
---
# <a name="day-function-visioshapesheet"></a>DAY Function (VisioShapeSheet)

Renvoie un integer, de 1 à 31, qui représente le jour dans _l’expression ou l’heure de date_. La fonction DAY utilise le calendrier grégorien.
  
## <a name="syntax"></a>Syntaxe

DAY( » ***datetime** _ « | _*_expression_*_ [, _ *_lcid_** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Obligatoire  <br/> |**String** <br/> |Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure. |
| _expression_ <br/> |Requis  <br/> |**String** <br/> |Toute expression qui génère une date et une heure. |
| _lcid_ <br/> |Facultatif  <br/> |**Number** <br/> |Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système. |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Tout composant d’heure  _dans l’heure ou_  _l’expression_ est ignoré. 
  
Aucun arrondissement n’est effectué. Si  _la date/_ heure est manquante ou ne peut pas être convertie en un résultat valide, la fonction renvoie une erreur. 
  
La fonction DAY accepte également une valeur de nombre unique pour  _l’expression_ où la partie nombre inte du résultat représente le nombre de jours depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

DAY("30 mai 1997 15:45:24")
  
Renvoie 30.
  
## <a name="example-2"></a>Exemple 2

DAY(DATEVALUE("30 mai 1997") + 7 je.)
  
Renvoie 6.
  
## <a name="example-3"></a>Exemple 3

DAY(35580.6337)
  
Renvoie 30.
  

