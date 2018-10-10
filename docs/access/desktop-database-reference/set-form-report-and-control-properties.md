---
title: Jeu de propriétés de formulaire, rapport et contrôle
TOCTitle: Set form, report, and control properties
ms:assetid: 03349d86-f107-9e49-89df-62f55f3a0735
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844789(v=office.15)
ms:contentKeyID: 48542977
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12286
f1_categories:
- Office.Version=v15
ms.openlocfilehash: f839ab2e2c6dfab32c49248f1be1878bf289eb6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470264"
---
# <a name="set-form-report-and-control-properties"></a>Jeu de propriétés de formulaire, rapport et contrôle

**S’applique à**: Access 2013 | Office 2013

Chaque formulaire, état, section et contrôle possède des paramètres de propriété que vous pouvez définir pour modifier l'aspect ou le fonctionnement de cet élément particulier. Vous pouvez afficher et modifier les propriétés à l'aide de la feuille des propriétés, d'une macro ou de Visual Basic.

## <a name="set-properties"></a>Définition des propriétés

1. En mode Création de formulaire ou d'état, sélectionnez le contrôle, la section, le formulaire ou l'état dont vous voulez définir la propriété. Vous pouvez sélectionner :
    
   - Un ou plusieurs contrôles. Pour sélectionner plusieurs contrôles, vous pouvez cliquer sur des contrôles en maintenant la touche Maj enfoncée ou vous pouvez cliquer et faire glisser le pointeur de la souris sur les contrôles à sélectionner. Si vous sélectionnez plusieurs contrôles, la feuille des propriétés n'affiche que les propriétés communes aux contrôles sélectionnés.
    
   - Une section. Cliquez sur le sélecteur de section de la section que vous voulez sélectionner.
    
   - Le formulaire ou l'état entier. Cliquez sur le sélecteur de formulaire ou le sélecteur d'état dans le coin supérieur du formulaire ou de l'état.

2. Affichez la feuille des propriétés en cliquant à l'aide du bouton droit de la souris sur l'objet ou la section, puis en cliquant sur **Propriétés** dans le menu contextuel ou en cliquant sur **Propriétés** dans la barre d'outils.

3. Cliquez sur la propriété dont vous voulez définir la valeur, puis exécutez une des actions suivantes :
    
   - Dans la zone de propriété, tapez le paramètre ou l'expression approprié.
    
   - Si la zone de propriété comporte une flèche, cliquez sur cette dernière et choisissez une valeur dans la liste.
    
   - Si un bouton **Générer** apparaît à droite de la zone de propriété, cliquez dessus pour afficher un générateur ou pour afficher une boîte de dialogue vous offrant un choix de générateurs. Par exemple, vous pouvez utiliser le Générateur de code, le Générateur de macro ou le Générateur de requêtes pour définir des propriétés.

## <a name="tips"></a>Conseils

- Microsoft Access comporte une zone de **Zoom** qui permet de taper et d'afficher des expressions ou d'autres paramètres de propriété longs. Pour afficher la zone de **Zoom**, cliquez sur une zone de propriété dans la feuille des propriétés. Ensuite, appuyez sur Maj+F2 ou cliquez sur le bouton droit de la souris et choisissez **Zoom** dans le menu contextuel.

- Vous pouvez définir la propriété **ControlSource** pour certains contrôles en tapant le paramètre de propriété dans le contrôle lui-même.

- Vous pouvez modifier les paramètres de propriété par défaut pour un type de contrôle de manière à ce que les contrôles que vous créez possèdent les nouveaux paramètres par défaut.

- Les paramètres de propriété d'un contrôle dépendant risquent de ne pas correspondre aux paramètres correspondants du champ de la table ou requête sous-jacente à laquelle le contrôle est associé. Si les paramètres sont différents, les paramètres du formulaire ou de l'état annulent généralement ceux de la table ou de la requête. Pour plus d'informations sur la manière dont les propriétés sont héritées, consultez la rubrique Comment les propriétés de contrôles sont liées aux propriétés de leurs champs sous-jacents.

