---
title: Formats de date et d’heure personnalisés pour la fonction Format (application web personnalisée Access)
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.assetid: f7d15fe6-bdad-4f1f-aa18-12a21fc111c4
description: Découvrez comment contrôler l’affichage d’une date ou d’une heure en créant une mise en forme personnalisée.
ms.localizationpriority: high
ms.openlocfilehash: 080c4a5d2b6b06fbc2dcfd996dbceaddcf175313
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62180039"
---
# <a name="custom-date-and-time-formats-for-the-format-function-access-custom-web-app"></a>Formats de date et d’heure personnalisés pour la fonction Format (application web personnalisée Access)

Découvrez comment contrôler l’affichage d’une date ou d’une heure en créant une mise en forme personnalisée.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="format-specifications"></a>Spécifications de format

Le tableau suivant répertorie les caractères que vous pouvez utiliser avec la fonction [Fonction de format (application web personnalisé de l'accès)](format-function-access-custom-web-app.md) pour créer des formats de date et d'heure personnalisés. 
  
|**Spécification de format**|**Description**|
|:-----|:-----|
|(:)  <br/> |Séparateur horaire. Dans certains paramètres régionaux, le séparateur horaire est représenté par d’autres caractères. Le séparateur horaire dissocie les heures, les minutes et les secondes lorsque des valeurs horaires sont mises en forme. Le caractère effectivement utilisé comme séparateur horaire dans la sortie mise en forme dépend de la valeur culturelle actuelle de votre application.  <br/> |
|(/)  <br/> |Séparateur de date. Dans certains paramètres régionaux, le séparateur de date est représenté par d’autres caractères. Le séparateur de date dissocie le jour, le mois et l’année lorsque des valeurs de date sont mises en forme. Le caractère effectivement utilisé comme séparateur de date dans la sortie mise en forme dépend de la culture actuelle de votre application.  <br/> |
|(%)  <br/> |Permet d’indiquer que le caractère suivant doit être lu en tant que format de lettre unique sans tenir compte des lettres de fin. Également utilisé pour indiquer qu’un format de lettre unique est lu en tant que format défini par l’utilisateur. Découvrez ce qui suit pour en savoir plus.  <br/> |
|d  <br/> |Affiche le jour sous la forme d’un nombre sans zéro non significatif (par exemple, 1). Utilisez %d s’il s’agit du seul caractère dans votre format numérique défini par l’utilisateur.  <br/> |
|dd  <br/> |Affiche le jour sous la forme d’un nombre avec un zéro non significatif (par exemple, 01).  <br/> |
|ddd  <br/> |Affiche le jour sous sa forme abrégée (par exemple, Dim).  <br/> |
|dddd  <br/> |Affiche le jour sous sa forme complète (par exemple, Dimanche).  <br/> |
|M  <br/> |Affiche le mois sous la forme d’un nombre sans zéro non significatif (par exemple, janvier est représenté par 1). Utilisez %M s’il s’agit du seul caractère dans votre format numérique défini par l’utilisateur.  <br/> |
|MM  <br/> |Affiche le mois sous la forme d’un nombre avec un zéro non significatif (par exemple, 01/12/01).  <br/> |
|MMM  <br/> |Affiche le mois sous sa forme abrégée (par exemple, Jan).  <br/> |
|MMMM  <br/> |Affiche le mois sous sa forme complète (par exemple, Janvier).  <br/> |
|gg  <br/> |Affiche la chaîne de période/ère (par exemple, APR. J.C.).  <br/> |
|h  <br/> |Affiche l’heure sous la forme d’un nombre sans zéro non significatif à l’aide de l’horloge au format 12 heures (par exemple, 1:15:15 PM). Utilisez %h s’il s’agit du seul caractère dans votre format numérique défini par l’utilisateur.  <br/> |
|hh  <br/> |Affiche l’heure sous la forme d’un nombre avec des zéros non significatifs à l’aide de l’horloge au format 12 heures (par exemple, 01:15:15 PM).  <br/> |
|H  <br/> |Affiche l’heure sous la forme d’un nombre sans zéro non significatif à l’aide de l’horloge au format 24 heures (par exemple, 1:15:15). Utilisez %H s’il s’agit du seul caractère dans votre format numérique défini par l’utilisateur.  <br/> |
|HH  <br/> |Affiche l’heure sous la forme d’un nombre avec des zéros non significatifs à l’aide de l’horloge au format 24 heures (par exemple, 01:15:15).  <br/> |
|m  <br/> |Affiche la minute sous la forme d’un nombre sans zéro non significatif (par exemple, 12:1:15). Utilisez %m s’il s’agit du seul caractère dans votre format numérique défini par l’utilisateur.  <br/> |
|mm  <br/> |Affiche les minutes sous la forme d’un nombre avec des zéros non significatifs (par exemple, 12:01:15).  <br/> |
|s  <br/> |Affiche les secondes sous la forme d’un nombre sans zéro non significatif (par exemple, 12:15:5). Utilisez %s s’il s’agit du seul caractère dans votre format numérique défini par l’utilisateur.  <br/> |
|ss  <br/> |Affiche les secondes sous la forme d’un nombre avec des zéros non significatifs (par exemple, 12:15:05).  <br/> |
|f  <br/> |Affiche des fractions de secondes. Par exemple, ff affiche les centièmes de secondes, tandis que ffff affiche les dix-millièmes de secondes. Vous pouvez utiliser jusqu’à 7 symboles f dans votre format défini par l’utilisateur. Utilisez %f s’il s’agit du seul caractère dans votre format numérique défini par l’utilisateur.  <br/> |
|t  <br/> |Affiche à l’aide du format 12 heures et avec l’indicateur A en majuscules pour une heure antérieure à midi et l’indicateur P en majuscules pour une heure située entre midi et 11:59 P.M. Utilisez %t s’il s’agit du seul caractère dans votre format numérique défini par l’utilisateur.  <br/> |
|tt  <br/> |Pour les paramètres régionaux faisant appel au format 12 heures avec l’indicateur AM en majuscules pour une heure antérieure à midi et l’indicateur PM en majuscules pour une heure située entre midi et 11:59 P.M.  <br/> Pour les paramètres régionaux faisant appel au format d’horloge de 24 heures, rien de s’affiche.  <br/> |
|y  <br/> |Affiche le numéro de l’année (0 à 9) sans zéro non significatif. Utilisez %y s’il s’agit du seul caractère dans votre format numérique défini par l’utilisateur.  <br/> |
|yy  <br/> |Affiche l’année dans un format numérique à deux chiffres avec un zéro non significatif, le cas échéant.  <br/> |
|yyy  <br/> |Affiche l’année dans un format numérique de quatre chiffres.  <br/> |
|yyyy  <br/> |Affiche l’année dans un format numérique de quatre chiffres.  <br/> |
||Affiche le décalage horaire sous la forme d’un nombre sans zéro non significatif (par exemple, -8). Utilisez %z s’il s’agit du seul caractère dans votre format numérique défini par l’utilisateur.  <br/> |
|z  <br/> |Affiche le décalage horaire sous la forme d’un nombre avec un zéro non significatif (par exemple, -08).  <br/> |
|zz  <br/> |Affiche le décalage horaire sous la forme d’un nombre avec un zéro non significatif (par exemple, -08).  <br/> |
|zzz  <br/> |Affiche le décalage de fuseau horaire complet (par exemple, -08:00)  <br/> |
   
## <a name="remarks"></a>Remarks

La mise en forme des chaînes respecte la casse. Une mise en forme différente peut être obtenue en utilisant une casse différente. Par exemple, lors de la mise en forme d’une valeur de date avec la chaîne « D », vous obtenez la date au format long (en fonction de vos paramètres régionaux actuels). Toutefois, si vous modifiez la casse en « d », vous obtenez la date au format court. En outre, des résultats inattendus ou une erreur peuvent se produire si la mise en forme prévue ne correspond pas à la casse d’une chaîne de format défini.
  
## <a name="see-also"></a>Voir aussi

- [Fonction de format (application web personnalisée Access)](format-function-access-custom-web-app.md) 
- [Formats numériques personnalisés pour la fonction Format (application web personnalisée Access)](custom-numeric-formats-for-the-format-function-access-custom-web-app.md)
  

