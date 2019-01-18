---
title: Définir des propriétés de formulaire, d’état et de contrôle
TOCTitle: Set form, report, and control properties
description: Chaque formulaire, état, section et contrôle possèdent des paramètres de propriété que vous pouvez définir pour modifier l’apparence ou le comportement d’un élément particulier dans Access 2013.
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: bacbdc100d147be8bf4327a5a775b199c79347bb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701689"
---
# <a name="set-form-report-and-control-properties"></a>Définir des propriétés de formulaire, d’état et de contrôle

**S’applique à**: Access 2013, Office 2013

Chaque formulaire, état, section et contrôle possède des paramètres de propriété que vous pouvez définir pour modifier l'aspect ou le fonctionnement de cet élément particulier. Vous pouvez afficher et modifier les propriétés à l'aide de la feuille des propriétés, d'une macro ou de Visual Basic.

## <a name="set-properties"></a>Définition des propriétés

1. En mode Création de formulaire ou d'état, sélectionnez le contrôle, la section, le formulaire ou l'état dont vous voulez définir la propriété. Vous pouvez sélectionner :
    
   - Un ou plusieurs contrôles. Pour sélectionner plusieurs contrôles, maintenez la touche MAJ enfoncée et sélectionnez les contrôles ou faites glisser le pointeur de la souris sur les contrôles que vous souhaitez sélectionner. Si vous sélectionnez plusieurs contrôles, la feuille des propriétés n'affiche que les propriétés communes aux contrôles sélectionnés.
    
   - Une section. Cliquez sur le sélecteur de section de la section que vous souhaitez sélectionner.
    
   - Le formulaire ou l'état entier. Cliquez sur le sélecteur de formulaire ou état dans le coin supérieur gauche du formulaire ou du rapport.

2. Afficher la feuille des propriétés, avec le bouton droit de l’objet ou la section, puis choisissez **Propriétés** dans le menu contextuel ou en cliquant sur **Propriétés** dans la barre d’outils.

3. Choisissez la propriété pour laquelle vous voulez définir la valeur, puis effectuez l’une des options suivantes :
    
   - Dans la zone de propriété, tapez le paramètre ou l'expression approprié.
    
   - Si la zone de propriété comporte une flèche, cliquez sur la flèche, puis choisissez une valeur dans la liste.
    
   - Si un bouton **Générer** apparaît à droite de la zone de propriété, cliquez dessus pour afficher un générateur ou pour afficher une boîte de dialogue vous offrant un choix de générateurs. Par exemple, vous pouvez utiliser le Générateur de code, le Générateur de macro ou le Générateur de requêtes pour définir des propriétés.

## <a name="tips"></a>Conseils

- Microsoft Access comporte une zone de **Zoom** qui permet de taper et d'afficher des expressions ou d'autres paramètres de propriété longs. Pour afficher la zone **Zoom** , choisissez une zone de propriété dans la feuille des propriétés. Appuyez sur MAJ + F2 ou avec le bouton droit, puis choisissez **Zoom** dans le menu contextuel.

- Vous pouvez définir la propriété **ControlSource** pour certains contrôles en tapant le paramètre de propriété dans le contrôle lui-même.

- Vous pouvez modifier les paramètres de propriété par défaut pour un type de contrôle de manière à ce que les contrôles que vous créez possèdent les nouveaux paramètres par défaut.

- Les paramètres de propriété d'un contrôle dépendant risquent de ne pas correspondre aux paramètres correspondants du champ de la table ou requête sous-jacente à laquelle le contrôle est associé. Si les paramètres sont différents, les paramètres du formulaire ou de l'état annulent généralement ceux de la table ou de la requête.

