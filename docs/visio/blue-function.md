---
title: BLUE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
ms.localizationpriority: medium
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: Renvoie le composant bleu d’une couleur. La valeur de retour est un nombre complet compris entre 0 et 255 inclus. La fonction renvoie 0 si l’entrée n’est pas valide.
ms.openlocfilehash: b510f739866b70670823418c8c6268e6d825e2ee
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776017"
---
# <a name="blue-function"></a>Fonction BLUE

Renvoie le composant bleu d’une couleur. La valeur de retour est un nombre complet compris entre 0 et 255 inclus. La fonction renvoie 0 si l’entrée n’est pas valide.
  
## <a name="syntax"></a>Syntaxe

BLUE(** *expression* ** ) 
  
### <a name="parameters"></a>Paramètres

|**Nom**|**Requis/Facultatif**|**Type de données**|**Description**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |Requis  <br/> |**String** <br/> |Index d’une couleur dans la table des couleurs d’un document, expression correspondant à une couleur personnalisée (telle que RVB ou TSL) ou référence à une cellule contenant un index ou un résultat de couleurs. |
   
### <a name="return-value"></a>Valeur renvoyée

Entier
  
## <a name="example-1"></a>Exemple 1

BLUE(Sheet.4! FillForegnd)
  
Renvoie la composante bleu de la couleur de remplissage de premier plan de Feuille.4.
  
## <a name="example-2"></a>Exemple 2

BLUE(13)
  
Renvoie 128 si le document utilise la palette de couleurs par défaut de Visio, où cyan est la couleur dont l’index est 13.
  
## <a name="example-3"></a>Exemple 3

BLUE(RGB(10, 20, 30))
  
Renvoie 30.
  

