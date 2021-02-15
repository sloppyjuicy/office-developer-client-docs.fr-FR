---
title: Boîte de dialogue Propriétés personnalisées d’un contrôle ActiveX
TOCTitle: ActiveX control custom properties dialog box
description: Cette boîte de dialogue des propriétés personnalisée propose une alternative à la liste des propriétés figurant dans la feuille des propriétés Microsoft Access pour définir les propriétés d'un contrôle ActiveX en mode Création.
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314104"
---
# <a name="activex-control-custom-properties-dialog-box"></a>Boîte de dialogue Propriétés personnalisées d’un contrôle ActiveX

**S’applique à** : Access 2013, Office 2013

Lors de la définition des propriétés d'un contrôle ActiveX, vous devrez ou souhaiterez peut-être utiliser la boîte de dialogue des propriétés personnalisée du contrôle. Cette boîte de dialogue des propriétés personnalisée propose une alternative à la liste des propriétés figurant dans la feuille des propriétés Microsoft Access pour définir les propriétés d'un contrôle ActiveX en mode Création de formulaire.

> [!NOTE]
> [!REMARQUE] Ces informations s'appliquent uniquement aux contrôles ActiveX dans un environnement de base de données Microsoft Access.

## <a name="two-ways-to-set-properties"></a>Deux façons de définir des propriétés

La raison d'être de la boîte de dialogue des propriétés personnalisée est que toutes les applications qui utilisent des contrôles ActiveX ne fournissent pas une feuille des propriétés comme Microsoft Access. La boîte de dialogue des propriétés personnalisée fournit une interface pour la définition des propriétés clés du contrôle sans tenir compte de l'interface fournie par l'application hôte.

Pour certaines propriétés de contrôle ActiveX, vous pouvez choisir un des deux endroits suivants pour définir la propriété :

- La feuille des propriétés Microsoft Access.
- La boîte de dialogue des propriétés personnalisée du contrôle ActiveX.

Dans certains cas, la boîte de dialogue des propriétés personnalisée est la seule manière de définir une propriété en mode Création. Cela est généralement le cas lorsque l'interface nécessaire pour définir une propriété ne fonctionne pas avec la feuille des propriétés de Microsoft Access. Par exemple, la propriété **GridFont** du contrôle Calendrier dispose d'un certain nombre d'éléments, mais vous ne pouvez en définir qu'un seul par propriété à l'aide de la feuille des propriétés de Microsoft Access.

## <a name="finding-the-custom-properties-dialog-box"></a>Recherche de la boîte de dialogue propriétés personnalisée

Tous les contrôles ActiveX ne fournissent pas une boîte de dialogue des propriétés personnalisée. Pour voir si un contrôle fournit cette boîte de dialogue des propriétés personnalisée, recherchez la propriété **Personnalisé** de ce contrôle dans la feuille des propriétés de Microsoft Access. Si la liste des propriétés contient le nom **Personnalisé,** le contrôle fournit la boîte de dialogue des propriétés personnalisées.

## <a name="using-the-custom-properties-dialog-box"></a>Utilisation de la boîte de dialogue propriétés personnalisée

Après avoir  choisi la zone Propriété personnalisée dans  la feuille des propriétés Microsoft Access, sélectionnez le bouton Créer à droite de la zone de propriétés pour afficher la boîte de dialogue des propriétés personnalisée du contrôle, souvent présentée sous la commande d’une boîte de dialogue à onglets. Choisissez l'onglet contenant l'interface permettant de définir les propriétés que vous souhaitez définir.

Après avoir apporté des modifications sur un onglet, vous  pouvez souvent appliquer ces modifications immédiatement en cliquant sur le bouton Appliquer (s’il est fourni). Vous pouvez choisir d’autres onglets pour définir d’autres propriétés selon vos besoins. Pour approuver toutes les modifications apportées dans la boîte de dialogue des propriétés personnalisées, sélectionnez le **bouton OK.** Pour revenir à la feuille des propriétés Microsoft Access sans modifier les paramètres de propriété, sélectionnez le **bouton** Annuler.

Vous pouvez également afficher la boîte de  dialogue des propriétés personnalisée en  choisissant la sous-commande Propriétés de la commande objet de contrôle ActiveX (par **exemple,** Objet Contrôle de calendrier) dans le **menu** Édition, ou en choisissant cette même sous-commande dans le menu raccourci du contrôle ActiveX. De plus, certaines propriétés dans la feuille des propriétés de Microsoft Access du contrôle ActiveX, comme la propriété **GridFontColor** du contrôle Calendrier, disposent d'un bouton **Générer** à droite de la zone des propriétés. Lorsque vous choisissez le **bouton Créer,** la boîte de dialogue des propriétés personnalisée s’affiche, avec l’onglet approprié sélectionné (par exemple, **Couleurs).**

