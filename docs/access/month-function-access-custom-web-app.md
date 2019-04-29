---
title: Fonction month (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Renvoie un entier qui représente le mois de la date spécifiée.
ms.openlocfilehash: 0ca7059a2fd6dad1f9790ad6f4eafe7affa014dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411490"
---
# <a name="month-function-access-custom-web-app"></a>Fonction month (application Web personnalisée Access)

Renvoie un entier qui représente le mois de la date spécifiée.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. ») > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

 **Mois** (*Date*) 
  
La fonction **Month** contient l'argument suivant. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Date*  <br/> |Expression qui peut être résolue en une valeur de date/heure.  <br/> |
   
## <a name="remarks"></a>Remarques

 **Month** renvoie la même valeur que **DatePart** (month, date). 
  
Si *Date* contient uniquement une partie d'heure, la valeur de retour est 1, le mois de base. 
  

