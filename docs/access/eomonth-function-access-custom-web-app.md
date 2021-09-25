---
title: EOMonth Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Renvoie le dernier jour du mois avant ou le nombre spécifié de mois.
ms.openlocfilehash: 6330865fa904fe2011d3cfaab988214950df51b9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601568"
---
# <a name="eomonth-function-access-custom-web-app"></a>EOMonth Function (Access custom web app)

Renvoie le dernier jour du mois avant ou le nombre spécifié de mois.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > Désolé, nous avons des problèmes de serveur, donc nous ne pouvons pas l’ajouter pour le *\<service\> moment. Veuillez essayer à nouveau plus tard.* > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

 **EOMonth** (*Date*, *NumberOfMonth*) 
  
**EOMonth contient** les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Date*  <br/> |Date de début au format Date/Heure ou dans une représentation texte acceptée d’une date.  <br/> |
| *NumberOfMonth*  <br/> |Nombre représentant le nombre de mois avant ou après la  *date*  .  <br/> |
   
## <a name="remarks"></a>Remarques

Si  *Date n’est*  pas une date valide, **EOMonth** renvoie une erreur. 
  
Si  *Date*  plus  *NumberOfMonth*  produit une date non valide, **EOMonth** renvoie une erreur. 
  

