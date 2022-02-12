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
ms.openlocfilehash: 021ccbb1fb0c6587e3d9b4b22558458de04bb878
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62777970"
---
# <a name="year-function-visioshapesheet"></a>YEAR Function (VisioShapeSheet)

Renvoie un entier qui représente l’année grégorien dans _l’heure ou l’expression_ _date/_ heure, mise en forme selon le style de date courte définie par les paramètres région et langue actuels du système.
  
## <a name="syntax"></a>Syntaxe

YEAR( » ***datetime** _ « | _*_expression_*_ [, _ *_lcid_** ])
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _datetime_ |Requis  |**String** | Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.  |
| _expression_ |Requis  |**Varie** |Toute expression qui génère une date et une heure.  |
| _lcid_ |Facultatif  |**Numérique** |Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.  |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="remarks"></a>Remarques

Le composant heure des arguments _datetime_ ou _expression_ n’est pas pris en compte.
  
Aucun arrondissement n’est effectué. Si _datetime_ est introuvable ou ne peut pas être interprété comme une date ou une heure valide, YEAR renvoie une erreur.
  
La fonction YEAR accepte également une valeur numérique simple pour l’argument _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899.
  
## <a name="example-1"></a>Exemple 1

YEAR(« 27/10/2007 13:45:24 »)
  
Renvoie 2007.
  
## <a name="example-2"></a>Exemple 2

YEAR(VALEURDATE("25 déc. 2006") + 7 je.)
  
Renvoie 2007.
  
## <a name="example-3"></a>Exemple 3

YEAR(35580.6337)
  
Renvoie 1997. 

