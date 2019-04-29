---
title: Fonction Year (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Renvoie une valeur numérique qui représente l'année de la date spécifiée dans le calendrier grégorien.
ms.openlocfilehash: 1400c352bcc070035d15b46f8e547e4637364299
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433121"
---
# <a name="year-function-access-custom-web-app"></a>Fonction Year (application Web personnalisée Access)

Renvoie une valeur numérique qui représente l'année de la date spécifiée dans le calendrier grégorien.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. ») > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

 **Année** (*Date*) 
  
La fonction **year** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Date*  <br/> |Expression qui peut être résolue en une valeur de date/heure. Expression de l'argument *Date* , expression de colonne, variable ou littéral de chaîne défini par l'utilisateur.  <br/> |
   
## <a name="remarks"></a>Remarques

Les valeurs renvoyées par les fonctions **year**, **Month**et **Day** seront des valeurs grégoriennes, quel que soit le format d'affichage de la valeur de date fournie. Par exemple, si le format d'affichage de la date fournie utilise le calendrier Hijri, les valeurs renvoyées pour les fonctions **year**, **Month**et **Day** seront des valeurs associées à la date grégorienne équivalente. 
  

