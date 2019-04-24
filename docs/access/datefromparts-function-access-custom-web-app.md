---
title: Fonction DateFromParts (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Renvoie une valeur de date pour l'année, le mois et le jour spécifiés.
ms.openlocfilehash: 7d47fe93d1990365f1db5885a3ea8fc056aabb9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282121"
---
# <a name="datefromparts-function-access-custom-web-app"></a>Fonction DateFromParts (application Web personnalisée Access)

Renvoie une valeur de date pour l'année, le mois et le jour spécifiés.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. ») > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

**DateFromParts** (*Année*, *mois*, *jour*) 
  
La fonction **DateFromParts** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Année*  <br/> |Expression de nombre entier spécifiant une année.  <br/> |
| *Month*  <br/> |Expression entière spécifiant un mois, comprise entre 1 et 12.  <br/> |
| *Day*  <br/> |Expression de nombre entier spécifiant un jour.  <br/> |
   
## <a name="remarks"></a>Remarques

**DateFromParts** renvoie une valeur date dont la partie date est définie sur l'année, le mois et le jour spécifiés, et la partie heure sur la valeur par défaut. Si les arguments ne sont pas valides, une erreur est générée. Si les arguments requis sont NULL, NULL est renvoyé. 
  
## <a name="example"></a>Exemple

L'expression suivante utilise la fonction **DateFromParts** pour calculer le premier jour du mois en cours. 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



