---
title: Equals(Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compare l’égalité de deux expressions.
ms.openlocfilehash: bbb1fb66561b1c55c4ea6e32c6d11be6514760ac
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180151"
---
# <a name="equals-access-custom-web-app"></a>Equals (Access custom web app)

Compare l’égalité de deux expressions.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

`= (Equals)`

*expression*   =   *expression* 
  
*expression*  représente toute expression valide. Si les expressions ne sont pas du même type de données, le type de données d’une expression doit être implicitement convertible en type de données de l’autre. La conversion varie en fonction des règles de priorité des types de données. 
  
## <a name="return-type"></a>Type renvoyé

**Boolean**
  
## <a name="remarks"></a>Remarques

Lorsque vous comparez deux expressions NULL, le résultat est TRUE.
  
La comparaison de null à une valeur non NULL se traduit toujours par FALSE.
  

