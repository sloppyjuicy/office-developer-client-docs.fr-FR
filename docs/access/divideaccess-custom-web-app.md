---
title: / (Divide) (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: Divise un nombre par un autre.
ms.openlocfilehash: 62775044a80aebab190763c37c7e5c72bced9503
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62179724"
---
# <a name="-divide-access-custom-web-app"></a>/ (Divide) (Application web personnalisée Access)

Divise un nombre par un autre.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
## <a name="syntax"></a>Syntaxe

 *2016*   /   *diviseur*
  
 *2016* Est l’expression numérique à diviser. Peut être n’importe quelle expression valide de l’un des types de données de la catégorie de type de données numériques, à l’exception du type de données date/heure.
  
 *Diviseur* Est l’expression numérique par laquelle diviser le versement. Peut être n’importe quelle expression valide de l’un des types de données de la catégorie de type de données numériques, à l’exception du type de données date/heure.
  
## <a name="return-type"></a>Type renvoyé

Renvoie le type de données de l’argument avec la priorité la plus élevée.
  
Si un nombre integer *est* divisé par un *diviseur d’un* nombre integer, le résultat est un nombre integer qui a une partie fractionnaire du résultat tronqué.
  
## <a name="remarks"></a>Remarques

La valeur réelle renvoyée par l’opérateur / est le quotient de la première expression divisée par la deuxième expression.
  