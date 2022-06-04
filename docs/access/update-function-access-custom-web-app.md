---
title: Update Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Retourne si une opération INSERT ou UPDATE a été tentée sur le champ spécifié.
ms.openlocfilehash: 03e04bef312b9b6140995e8d78cdf0a777caeae5
ms.sourcegitcommit: eb83b72d14a07ac316c71e8208397d1c7046f6df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2022
ms.locfileid: "65893962"
---
# <a name="update-function-access-custom-web-app"></a>Update Function (Access custom web app)

Retourne si une opération INSERT ou UPDATE a été tentée sur le champ spécifié.
  
> [!NOTE]
> La fonctionnalité de stockage dans le cloud décrite dans cet article n'est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l'erreur suivante : *Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas ajouter\<service\> en ce moment. Veuillez réessayer plus tard.*
> Pour le stockage cloud pour Office Online, Office pour iOS et Office pour Android, recherchez notre programme [Office cloud Stockage partenaire.](/microsoft-365/cloud-storage-partner-program/)
  
## <a name="syntax"></a>Syntaxe

 **Mise à jour** (*colonne*)
  
La fonction **Update** contient les arguments suivants.
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Colonne*  <br/> |Nom du champ à vérifier pour une opération INSERT ou UPDATE. |
   

## <a name="remarks"></a>Remarques

La fonction **Update** retourne TRUE, qu’une tentative INSERT ou UPDATE soit réussie.
  