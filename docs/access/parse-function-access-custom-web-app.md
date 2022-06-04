---
title: Analyser la fonction (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analyse une valeur de texte et retourne sa valeur dans un type donné à l’aide de la culture de l’application.
ms.openlocfilehash: b52c43dd612ac7b2e07a8da244c4ba600b0e8888
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65894613"
---
# <a name="parse-function-access-custom-web-app"></a>Analyser la fonction (application web personnalisée Access)

Analyse une valeur de texte et retourne sa valeur dans un type donné à l’aide de la culture de l’application.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](/microsoft-365/cloud-storage-partner-program/)
  
## <a name="syntax"></a>Syntaxe

**Analyse** (*TextExpression*, *DataType*)
  
La fonction **Analyse** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Expression de texte représentant la valeur mise en forme à analyser dans le type de données spécifié. |
| *DataType*  <br/> |Valeur littérale représentant le type de données demandé pour le résultat. |
   
## <a name="remarks"></a>Remarques

Utilisez **l’analyse** uniquement pour la conversion de chaîne en types date/heure et nombre. Pour les conversions de type général, utilisez la fonction **Convert** . N’oubliez pas qu’il existe une certaine surcharge de performances lors de l’analyse de la valeur de chaîne.
  