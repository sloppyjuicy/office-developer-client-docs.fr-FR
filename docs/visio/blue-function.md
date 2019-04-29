---
title: BLUE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
localization_priority: Normal
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: Renvoie la composante bleu d'une couleur. La valeur renvoyée est un entier compris entre 0 et 255 (inclus). La fonction renvoie 0 si l’entrée n’est pas valide.
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439036"
---
# <a name="blue-function"></a>Fonction BLUE

Renvoie la composante bleu d'une couleur. La valeur renvoyée est un entier compris entre 0 et 255 (inclus). La fonction renvoie 0 si l’entrée n’est pas valide.
  
## <a name="syntax"></a>Syntaxe

BLEU (* * *expression* * *) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Obligatoire  <br/> |**String** <br/> |Index d’une couleur dans la table des couleurs d’un document, expression correspondant à une couleur personnalisée (telle que RVB ou TSL) ou référence à une cellule contenant un index ou un résultat de couleurs.  <br/> |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="example-1"></a>Exemple 1

BLEU (feuille. 4! FillForegnd
  
Renvoie la composante bleu de la couleur de remplissage de premier plan de Feuille.4.
  
## <a name="example-2"></a>Exemple 2

BLEU (13)
  
Renvoie 128 si le document utilise la palette de couleurs par défaut de Visio, où cyan est la couleur dont l’index est 13.
  
## <a name="example-3"></a>Exemple 3

BLUE(RGB(10, 20, 30))
  
Renvoie 30.
  

