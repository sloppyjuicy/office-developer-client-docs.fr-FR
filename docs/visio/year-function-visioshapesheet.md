---
title: YEAR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
ms.localizationpriority: medium
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Renvoie un entier qui représente l’année grégorien dans l’heure ou l’expression date/heure, mise en forme selon le style de date courte définie par les paramètres région et langue actuels du système.
ms.openlocfilehash: 156791dde6af8858b3eeaab643c38762811cac4a
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462550"
---
# <a name="year-function-visioshapesheet"></a>YEAR Function (VisioShapeSheet)

Renvoie un entier qui représente l’année grégorien dans _l’heure ou l’expression_ _date/_ heure, mise en forme selon le style de date courte définie par les paramètres région et langue actuels du système.
  
## <a name="syntax"></a>Syntaxe

YEAR( » ***datetime** _ « | _*_expression_*_ [, _ *_lcid_** ]) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |Requis  <br/> |**String** <br/> | Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  <br/> |
| _expression_ <br/> |Requis  <br/> |**Varie** <br/> |Toute expression qui génère une date et une heure.  <br/> |
| _lcid_ <br/> |Facultatif  <br/> |**Numérique** <br/> |Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Le composant d’heure  _dans l’heure ou_  _l’expression_ est ignoré. 
  
Aucun arrondissement n’est effectué. Si  _date/heure_ est manquante ou ne peut pas être interprétée comme une date ou une heure valide, YEAR renvoie une erreur. 
  
La fonction YEAR accepte également une valeur de nombre unique pour  _l’expression_ où la partie nombre inte du résultat représente le nombre de jours depuis le 30 décembre 1899. 
  
## <a name="example-1"></a>Exemple 1

YEAR(« 27/10/2007 13:45:24 »)
  
Renvoie 2007.
  
## <a name="example-2"></a>Exemple 2

YEAR(VALEURDATE("25 déc. 2006") + 7 je.)
  
Renvoie 2007.
  
## <a name="example-3"></a>Exemple 3

YEAR(35580.6337)
  
Renvoie 1997.
  

