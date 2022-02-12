---
title: Update Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Renvoie si une tentative d’opération INSERT ou UPDATE a été tentée sur le champ spécifié.
ms.openlocfilehash: 7c0dd0494369f900bafc6f2cf5e27df08e025c15
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62776745"
---
# <a name="update-function-access-custom-web-app"></a>Update Function (Access custom web app)

Renvoie si une tentative d’opération INSERT ou UPDATE a été tentée sur le champ spécifié.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](https://dev.office.com/programs/officecloudstorage)
  
## <a name="syntax"></a>Syntaxe

 **Mise à** jour (*colonne*)
  
La **fonction Update** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Colonne*  <br/> |Nom du champ à vérifier pour une opération INSERT ou UPDATE. |
   

## <a name="remarks"></a>Remarques

La **fonction Update** renvoie TRUE, qu’une tentative INSERT ou UPDATE réussisse ou non.
  