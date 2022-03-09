---
title: ChangeView Macro Action (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7eb20f21-0218-4a2c-9bbc-90218a1e87bc
description: Vous pouvez utiliser l’action ChangeView pour naviguer entre les vues en place.
ms.openlocfilehash: f0f6f8d540818bdcf0e71265f400079a74f38646
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370498"
---
# <a name="changeview-macro-action-access-custom-web-app"></a>ChangeView Macro Action (Application web personnalisée Access)

Vous pouvez utiliser l’action **ChangeView** pour naviguer entre les vues en place.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.
  
## <a name="setting"></a>Paramètre

**L’action ChangeView** a les arguments suivants.
  
|**Argument de l'action**|**Obligatoire**|**Description**|
|:-----|:-----|:-----|
|Tableau  <br/> |Oui  <br/> |Nom de la table à ouvrir. |
|Afficher  <br/> |Oui  <br/> |Nom de la vue à ouvrir. |
|Où  <br/> |Non  <br/> |Spécifié, remplace la condition Where de la source de l'enregistrement de l'objet. |
|Trier par  <br/> |Non  <br/> |Une expression de chaîne qui inclut le nom du champ ou des champs à partir desquels trier les enregistrements et les mots clés ASC ou DESC facultatifs. Par défaut, cet argument est vide. |

## <a name="remarks"></a>Remarques

Tout tri ou filtrage appliqué par l’utilisateur est effacé lorsque l’action **ChangeView** est appelée.
  
*L’argument OrderBy* est le nom du ou des champs sur lesquels vous souhaitez trier les enregistrements. Lorsque vous utilisez plusieurs noms de champs, séparez-les par une virgule (,).
  
Lorsque vous définissez *l’argument OrderBy* , les enregistrements sont triés par défaut dans l’ordre croissant.
  