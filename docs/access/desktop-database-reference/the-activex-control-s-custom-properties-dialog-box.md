---
title: Boîte de dialogue Propriétés personnalisées d’un contrôle ActiveX
TOCTitle: ActiveX control custom properties dialog box
description: Cette boîte de dialogue des propriétés personnalisée propose une alternative à la liste des propriétés figurant dans la feuille des propriétés Microsoft Access pour définir les propriétés d'un contrôle ActiveX en mode Création de formulaire.
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f4574abc86e6eacd38721e601d26c8b8fbf0a0d3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712133"
---
# <a name="activex-control-custom-properties-dialog-box"></a>Boîte de dialogue Propriétés personnalisées d’un contrôle ActiveX

**S’applique à**: Access 2013, Office 2013

Lors de la définition des propriétés d'un contrôle ActiveX, vous devrez ou souhaiterez peut-être utiliser la boîte de dialogue des propriétés personnalisée du contrôle. Cette boîte de dialogue des propriétés personnalisée propose une alternative à la liste des propriétés figurant dans la feuille des propriétés Microsoft Access pour définir les propriétés d'un contrôle ActiveX en mode Création de formulaire.

> [!NOTE]
> [!REMARQUE] Ces informations s'appliquent uniquement aux contrôles ActiveX dans un environnement de base de données Microsoft Access.

## <a name="two-ways-to-set-properties"></a>Deux manières de définir des propriétés

La raison d'être de la boîte de dialogue des propriétés personnalisée est que toutes les applications qui utilisent des contrôles ActiveX ne fournissent pas une feuille des propriétés comme Microsoft Access. La boîte de dialogue des propriétés personnalisée fournit une interface pour la définition des propriétés clés du contrôle sans tenir compte de l'interface fournie par l'application hôte.

Pour certaines propriétés de contrôle ActiveX, vous pouvez choisir un des deux endroits suivants pour définir la propriété :

- La feuille des propriétés Microsoft Access.
- La boîte de dialogue des propriétés personnalisée du contrôle ActiveX.

Dans certains cas, la boîte de dialogue des propriétés personnalisée est la seule manière de définir une propriété en mode Création. Cela est généralement le cas lorsque l'interface nécessaire pour définir une propriété ne fonctionne pas avec la feuille des propriétés de Microsoft Access. Par exemple, la propriété **GridFont** du contrôle Calendrier dispose d'un certain nombre d'éléments, mais vous ne pouvez en définir qu'un seul par propriété à l'aide de la feuille des propriétés de Microsoft Access.

## <a name="finding-the-custom-properties-dialog-box"></a>Recherche de la boîte de dialogue Propriétés personnalisées

Tous les contrôles ActiveX ne fournissent pas une boîte de dialogue des propriétés personnalisée. Pour voir si un contrôle fournit cette boîte de dialogue des propriétés personnalisée, recherchez la propriété **Personnalisé** de ce contrôle dans la feuille des propriétés de Microsoft Access. Si la liste des propriétés contient le nom **personnalisé**, le contrôle fournit la boîte de dialogue Propriétés personnalisées.

## <a name="using-the-custom-properties-dialog-box"></a>À l’aide de la boîte de dialogue Propriétés personnalisées

Une fois que vous choisissez la zone de propriété **personnalisée** dans la feuille des propriétés Microsoft Access, cliquez sur le bouton **Générer** à droite de la zone de propriété pour afficher la boîte de dialogue des propriétés personnalisées du contrôle, souvent présentée en tant qu’une boîte de dialogue à onglets. Choisissez l'onglet contenant l'interface permettant de définir les propriétés souhaitées.

Après avoir apporté des modifications dans un onglet, vous pouvez souvent les appliquer immédiatement en cliquant sur le bouton **Appliquer** (le cas échéant). Vous pouvez choisir les autres onglets pour définir les autres propriétés selon vos besoins. Pour approuver toutes les modifications apportées dans la boîte de dialogue Propriétés personnalisées, choisissez le bouton **OK** . Pour revenir à la feuille des propriétés Microsoft Access sans modifier les paramètres de propriété, cliquez sur le bouton **Annuler** .

Vous pouvez également afficher la boîte de dialogue des propriétés personnalisées en cliquant sur la sous-commande **Propriétés** du contrôle ActiveX **objet** , commande (par exemple, l' **Objet de contrôle calendrier**) dans le menu **Edition** , ou en sélectionnant la même sous-commande sur le menu contextuel pour le contrôle ActiveX. De plus, certaines propriétés dans la feuille des propriétés de Microsoft Access du contrôle ActiveX, comme la propriété **GridFontColor** du contrôle Calendrier, disposent d'un bouton **Générer** à droite de la zone des propriétés. Lorsque vous choisissez le bouton **Générer** , la boîte de dialogue Propriétés personnalisées s’affiche avec l’onglet approprié est sélectionné (par exemple, des **couleurs**).

