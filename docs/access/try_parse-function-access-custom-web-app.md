---
title: Fonction Try_Parse (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analyse une valeur de texte dans le type de données spécifié dans la culture de l'application ou renvoie la valeur null si la conversion n'est pas valide.
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307797"
---
# <a name="tryparse-function-access-custom-web-app"></a>Fonction Try_Parse (application Web personnalisée Access)

Analyse une valeur de texte dans le type de données spécifié dans la culture de l'application ou renvoie la valeur null si la conversion n'est pas valide.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. ») > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

 **Try_Parse** (*TextExpression*, *DataType*) 
  
La fonction **Try_Parse** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Expression de texte représentant la valeur mise en forme à analyser dans le type de données spécifié.  <br/> |
| *DataType*  <br/> |Le type de données dans lequel analyser *TextExpression* .  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez **Try_Parse** uniquement pour convertir une chaîne en type de date/heure et de nombre. Pour les conversions de type générales, continuez à utiliser **Convert**. 
  

