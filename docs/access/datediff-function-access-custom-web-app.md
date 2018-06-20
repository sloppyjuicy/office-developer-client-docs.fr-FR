---
title: Fonction DateDiff (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Renvoie le nombre de limites composant date spécifiée comprises entre la date de début et date de fin.
ms.openlocfilehash: fe898ec5eb59cb341250cb0c0e2e35bc55d37eb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781838"
---
# <a name="datediff-function-access-custom-web-app"></a>Fonction DateDiff (accès personnalisé web app)

Renvoie le nombre de limites composant date spécifiée comprises entre la date de début et date de fin.
  
> [!NOTE]
> La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.* > Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

**DateDiff** (*DatePart*, *StartDate*, *EndDate*) 
  
La fonction **DateDiff** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *DatePart*  <br/> |Est la partie de *StartDate* et *EndDate* qui spécifie le type de limite franchi. Reportez-vous à la section Remarques pour la liste des paramètres valides.  <br/> |
| *Date de début*  <br/> |Une expression qui peut être résolue sur une valeur de Date/heure. La *Date argument* , l’expression de colonne, variable définie par l’utilisateur ou une expression chaîne littérale.  <br/> |
| *Date de fin*  <br/> |Une expression qui peut être résolue sur une valeur de Date/heure. La *Date argument* , l’expression de colonne, variable définie par l’utilisateur ou une expression chaîne littérale.  <br/> |
   
## <a name="remarks"></a>Remarques

Le tableau suivant répertorie tous les arguments *DatePart* valides. 
  
|***DatePart***|
|:-----|
|**year** <br/> |
|**trimestre** <br/> |
|**Mois** <br/> |
|**DAYOFYEAR** <br/> |
|**day** <br/> |
|**semaine** <br/> |
|**heure** <br/> |
|**minute** <br/> |
|**seconde** <br/> |
|**milliseconde** <br/> |
   

