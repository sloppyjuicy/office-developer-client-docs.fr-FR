---
title: Fonction DateWithTimeFromParts (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Renvoie une date et une heure basées sur une année, un mois, un jour et une heure spécifiés.
ms.openlocfilehash: ee995d346ca27e683f342cf3f611c1147997d24e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422088"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a>Fonction DateWithTimeFromParts (application Web personnalisée Access)

Renvoie une date et une heure basées sur une année, un mois, un jour et une heure spécifiés.
  
> [!NOTE]
> La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. ») > En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

**DateWithTimeFromParts** (*Année*, *mois*, *jour*, *heure*, *minute*, *seconde*) 
  
La fonction **DateWithTimeFromParts** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *Année*  <br/> |Expression de nombre entier spécifiant une année.  <br/> |
| *Month*  <br/> |Expression de nombre entier spécifiant un mois.  <br/> |
| *Day*  <br/> |Expression de nombre entier spécifiant un jour.  <br/> |
| *Hour*  <br/> |Expression de type Integer qui spécifie les heures.  <br/> |
| *Minute*  <br/> |Expression de nombre entier spécifiant des minutes.  <br/> |
| *Second*  <br/> |Expression de type Integer qui spécifie les secondes.  <br/> |
   
## <a name="remarks"></a>Remarques

**DateWithTimeFromParts** renvoie une valeur date/heure entièrement initialisée. Si les arguments ne sont pas valides, une erreur est générée. Si les arguments requis sont NULL, NULL est renvoyé. 
  

