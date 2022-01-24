---
title: ChangeView Macro Action (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Vous pouvez utiliser l’action ChangeView pour naviguer entre les vues en place.
ms.openlocfilehash: d595e13259b6950009da5502d35647c623b8aeea
ms.sourcegitcommit: 2411ec8262cd0ed92f8a072fb53b51e3e496d49e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/24/2022
ms.locfileid: "62179780"
---
# <a name="changeview-macro-action-access-custom-web-app"></a>ChangeView Macro Action (Application web personnalisée Access)

Vous pouvez utiliser l’action **ChangeView** pour naviguer entre les vues en place.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
## <a name="setting"></a>Paramètre

**L’action ChangeView** a les arguments suivants.
  
|**Argument de l'action**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
|Tableau  <br/> |Oui  <br/> |Nom de la table à ouvrir.  <br/> |
|Afficher  <br/> |Oui  <br/> |Nom de la vue à ouvrir.  <br/> |
|Où  <br/> |Non  <br/> |Spécifié, remplace la condition Where de la source de l'enregistrement de l'objet.  <br/> |
|Trier par  <br/> |Non  <br/> |Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs. Par défaut, cet argument est vide.  <br/> |

## <a name="remarks"></a>Remarques

Tout tri ou filtrage appliqué par l’utilisateur est effacé lorsque l’action **ChangeView** est appelée.
  
*L’argument OrderBy* est le nom du ou des champs sur lesquels vous souhaitez trier les enregistrements. Lorsque vous utilisez plusieurs noms de champs, séparez-les par une virgule (,).
  
Lorsque vous définissez *l’argument OrderBy,* les enregistrements sont triés par défaut dans l’ordre croissant.
  