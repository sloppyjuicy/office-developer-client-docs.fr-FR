---
title: Fonction Try_Parse (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analyse d’une valeur de texte pour le type de données spécifié dans la culture de l’application ou renvoie la valeur Null si la conversion n’est pas valide.
ms.openlocfilehash: 3446e928d9772641f9aea7b956e142f995824b1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782002"
---
# <a name="tryparse-function-access-custom-web-app"></a>Fonction Try_Parse (accès personnalisé web app)

Analyse d’une valeur de texte pour le type de données spécifié dans la culture de l’application ou renvoie la valeur Null si la conversion n’est pas valide.
  
> [!NOTE]
> La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.* > Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage). 
  
## <a name="syntax"></a>Syntaxe

 **Try_Parse** (*TextExpression*, *type de données*) 
  
La fonction **Try_Parse** contient les arguments suivants. 
  
|**Nom de l’argument**|**Description**|
|:-----|:-----|
| *TextExpression*  <br/> |Une expression de texte représentant la valeur mise en forme à analyser dans le type de données spécifié.  <br/> |
| *DataType*  <br/> |Le type de données dans lequel analyser *TextExpression* .  <br/> |
   
## <a name="remarks"></a>Remarques

Utilisez **Try_Parse** uniquement pour réaliser la conversion d’une chaîne de date/heure et types de numéros. Pour les conversions de type général, continuer à utiliser à **convertir**. 
  

