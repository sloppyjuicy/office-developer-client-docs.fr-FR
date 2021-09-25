---
title: À propos des valeurs Date, Heure et Durée
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251852
ms.localizationpriority: medium
ms.assetid: b6951a92-f32a-5829-5e07-b277b7934df3
description: Vous pouvez effectuer des opérations dans les formules à l’aide de valeurs de date, d’heure et de durée. Dans Microsoft Visio, une expression de date et d’heure peut être évaluée comme une valeur simple. Une expression de date et d’heure est toute expression reconnue en tant que date et/ou heure ou référence à une cellule contenant une date et/ou une heure. Cette expression peut contenir des chaînes et des nombres avec un format de date et d’heure ainsi que des valeurs de date et d’heure renvoyées par des fonctions.
ms.openlocfilehash: c991a10c1403009b2abb5719d37946469e591c82
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554942"
---
# <a name="about-date-time-and-duration-values"></a>À propos des valeurs Date, Heure et Durée

Vous pouvez effectuer des opérations dans les formules à l’aide de valeurs de date, d’heure et de durée. Dans Microsoft Visio, une expression de date et d’heure peut être évaluée comme une valeur simple. Une expression de date et d’heure est toute expression reconnue en tant que date et/ou heure ou référence à une cellule contenant une date et/ou une heure. Cette expression peut contenir des chaînes et des nombres avec un format de date et d’heure ainsi que des valeurs de date et d’heure renvoyées par des fonctions.
  
Dans Visio, les valeurs de date et d'heure sont enregistrées en interne sous la forme de nombres à virgule flottante de 64 bits. La valeur à gauche du séparateur décimal représente le nombre de jours depuis le 31 décembre 1899. La valeur à droite du séparateur décimal représente la fraction du jour depuis minuit. Midi est représenté par 0,5.
  
Pour utiliser des dates et des heures dans une expression (plutôt qu'une constante), vous devez employer la fonction appropriée afin de les identifier en tant que valeurs de date et d'heure.
  
## <a name="valid-dates"></a>Dates correctes

||||
|:-----|:-----|:-----|
| "2/28"  <br/> | "2/28/99"  <br/> | "2/28/1999"  <br/> |
| "2-28"  <br/> | "2-28-99"  <br/> | "2-28/1999"  <br/> |
| "6 mar 99"  <br/> | "6 mar"  <br/> | "6 mar 99"  <br/> |
| "1 janvier 99"  <br/> | "1 jan 99"  <br/> | "1 jan 1999"  <br/> |
| "Jan 00"  <br/> | "Janvier 2000"  <br/> | "1 jan 00"  <br/> |
   
## <a name="valid-times"></a>Heures correctes

||||
|:-----|:-----|:-----|
| "3:45"  <br/> | "3:45:27"  <br/> | « 7a »  <br/> |
| "7 am"  <br/> | "7 p"  <br/> | "7:30 PM"  <br/> |
   
## <a name="date-and-time-functions"></a>Fonctions Date et Heure

|**Fonction**|**Description**|
|:-----|:-----|
|[DATE](date-function-visioshapesheet.md) <br/> | Convertit un nombre en valeur de date.  <br/> |
|[DATETIME](datetime-function.md) <br/> | Convertit une chaîne en valeur de date et d'heure.  <br/> |
|[DATEVALUE](datevalue-function-visioshapesheet.md) <br/> | Convertit une chaîne en valeur de date.  <br/> |
|[NOW](now-function-visioshapesheet.md) <br/> | Renvoie la date système actuelle sous forme de valeur de date et d'heure.  <br/> |
|[TIME](time-function-visioshapesheet.md) <br/> | Convertit un nombre en valeur d'heure.  <br/> |
|[TIMEVALUE](timevalue-function-visioshapesheet.md) <br/> | Convertit une chaîne en valeur d'heure.  <br/> |
|[JOUR](day-function-visioshapesheet.md) <br/> | Renvoie le jour d'une expression de date et d'heure.  <br/> |
|[DAYOFYEAR](dayofyear-function.md) <br/> | Renvoie le jour de l'année d'une expression de date et d'heure.  <br/> |
|[HEURE](hour-function-visioshapesheet.md) <br/> | Renvoie l'heure d'une expression de date et d'heure.  <br/> |
|[MINUTE](minute-function-visioshapesheet.md) <br/> | Renvoie les minutes d'une expression de date et d'heure.  <br/> |
|[MONTH](month-function-visioshapesheet.md) <br/> | Renvoie le mois d'une expression de date et d'heure.  <br/> |
|[SECOND](second-function-visioshapesheet.md) <br/> | Renvoie les secondes d'une expression de date et d'heure.  <br/> |
|[WEEKDAY](weekday-function-visioshapesheet.md) <br/> | Renvoie le numéro du jour de la semaine d'une expression de date et d'heure.  <br/> |
|[YEAR](year-function-visioshapesheet.md) <br/> | Renvoie l'année d'une expression de date et d'heure.  <br/> |
   
## <a name="duration"></a>Durée

Vous pouvez effectuer des opérations permettant de calculer une durée ou un temps écoulé. La durée est enregistrée en interne sous forme de jours et de fractions de jour. Par exemple, 1 semaine, 7 jours et 168 heures écoulés sont tous représentés par le nombre 7,0 mais s'affichent avec les unités appropriées.
  
Visio gère les unités de durée du tableau suivant.
  
|**Unit**|**Abréviation**|**Abréviation universelle**|
|:-----|:-----|:-----|
| jour écoulé  <br/> | JOURE, JE.  <br/> | non  <br/> |
| heure écoulée  <br/> | HEUREE, HE.  <br/> | eh  <br/> |
| minute écoulée  <br/> | MINUTEE, ME.  <br/> | em  <br/> |
| seconde écoulée  <br/> | SECONDEE, SE.  <br/> | es  <br/> |
| semaine écoulée  <br/> | SEMAINEE, WE.  <br/> | ew  <br/> |
   
Vous pouvez ajouter une date et une heure à une durée afin de calculer une nouvelle date et heure. Vous pouvez effectuer les opérations du tableau ci-dessous à l'aide de dates, d'heures et de durées.
  
|**Entrée**|**Résultat**|
|:-----|:-----|
| Date-heure +/- durée  <br/> | Valeur de date et d'heure  <br/> |
| Durée +/- date-heure  <br/> | Valeur de date et d'heure  <br/> |
| Durée +/- durée  <br/> | Valeur de durée  <br/> |
| Date-heure + date-heure  <br/> | Valeur de date et d'heure  <br/> |
| Date-heure - date-heure  <br/> | Valeur de durée  <br/> |
   

