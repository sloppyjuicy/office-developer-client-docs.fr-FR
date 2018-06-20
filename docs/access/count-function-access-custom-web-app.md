---
title: Fonction Count (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Renvoie le nombre d’enregistrements dans une table ou requête.
ms.openlocfilehash: 300fcbfd2aa927dd19516355ae28eec2adadf521
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781835"
---
# <a name="count-function-access-custom-web-app"></a>Fonction Count (accès personnalisé web app)

Renvoie le nombre d’enregistrements dans une table ou requête.
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

**Nombre** (*Expression*) 
  
La fonction **Count** contient l’argument suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Expression*  <br/> |Expression chaîne identifiant le champ qui contient les données que vous souhaitez nombre ou une expression qui effectue un calcul en utilisant les données du champ. Les opérandes de *l’Expression* peuvent inclure le nom d’un champ de table ou d’une fonction (qui peut être intrinsèque ou définie par l’utilisateur, mais pas d’autres SQL fonctions d’agrégation). Vous pouvez compter tous les types de données, y compris du texte.  <br/> |
   
## <a name="remarks"></a>Notes

Vous pouvez utiliser Count pour compter le nombre d’enregistrements dans une requête sous-jacente. Par exemple, vous pouvez utiliser Count pour compter le nombre de commandes expédiées vers un pays ou une région.
  
**Nombre** (\*) renvoie le nombre d’éléments dans un groupe. Cela inclut les valeurs NULL et les doublons. 
  

