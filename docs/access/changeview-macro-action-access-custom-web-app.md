---
title: ChangeView, action de macro (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Vous pouvez utiliser l'action ChangeView pour naviguer entre les vues en place.
ms.openlocfilehash: 0c1e27c264a826d38ec2efbd5be9bc6237ad7437
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425357"
---
# <a name="changeview-macro-action-access-custom-web-app"></a>ChangeView, action de macro (application Web personnalisée Access)

Vous pouvez utiliser l'action **ChangeView** pour naviguer entre les vues en place. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="setting"></a>Paramètre

L'action **ChangeView** utilise les arguments suivants. 
  
|**Argument de l'action**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
|Table  <br/> |Oui  <br/> |Nom de la table à ouvrir.  <br/> |
|View  <br/> |Oui  <br/> |Nom de la vue à ouvrir.  <br/> |
|Où  <br/> |Non  <br/> |Spécifié, remplace la condition Where de la source de l'enregistrement de l'objet.  <br/> |
|Trier par  <br/> |Non  <br/> |Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs. Par défaut, cet argument est vide.  <br/> |
   
## <a name="remarks"></a>Remarques

Tout tri ou filtrage appliqué par l'utilisateur est effacé lors de l'appel de l'action **ChangeView** . 
  
L'argument *orderby* est le nom du ou des champs sur lesquels vous souhaitez trier les enregistrements. Lorsque vous utilisez plusieurs noms de champs, séparez-les par une virgule (,). 
  
Lorsque vous définissez l'argument *orderby* , les enregistrements sont triés par défaut dans l'ordre croissant. 
  

