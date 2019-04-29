---
title: Fonction EOMonth (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Renvoie le dernier jour du mois précédent ou spécifié.
ms.openlocfilehash: 87a837069be223fdd2f9c809d706782e0955e2aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437454"
---
# <a name="eomonth-function-access-custom-web-app"></a>Fonction EOMonth (application Web personnalisée Access)

Renvoie le dernier jour du mois précédent ou spécifié.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. ») > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

 **EOMonth** (*Date*, *NumberOfMonth*) 
  
L' **EOMonth** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Date*  <br/> |Date de début dans le format date/heure ou dans une représentation textuelle acceptée d'une date.  <br/> |
| *NumberOfMonth*  <br/> |Nombre représentant le nombre de mois avant ou après la *Date* .  <br/> |
   
## <a name="remarks"></a>Remarques

Si *Date* n'est pas une date valide, **EOMonth** renvoie une erreur. 
  
Si *Date* plus *NumberOfMonth* génère une date non valide, **EOMonth** renvoie une erreur. 
  

