---
title: Update Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Renvoie si une tentative d’opération INSERT ou UPDATE a été tentée sur le champ spécifié.
ms.openlocfilehash: 0ec2576a95c76be2f61abbd59c7de098a160c279
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614646"
---
# <a name="update-function-access-custom-web-app"></a>Update Function (Access custom web app)

Renvoie si une tentative d’opération INSERT ou UPDATE a été tentée sur le champ spécifié.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas l’ajouter pour le *\<service\> moment. Veuillez essayer à nouveau plus tard.* > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

 **Update** (*Column*) 
  
La **fonction Update** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Colonne*  <br/> |Nom du champ à vérifier pour une opération INSERT ou UPDATE.  <br/> |
   
## <a name="remarks"></a>Remarques

La **fonction Update** renvoie TRUE, qu’une tentative INSERT ou UPDATE réussisse ou non. 
  

