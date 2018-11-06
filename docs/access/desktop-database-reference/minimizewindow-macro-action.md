---
title: MinimizeWindow, action de macro
TOCTitle: MinimizeWindow macro action
ms:assetid: 3a92b654-15ce-1ed1-63e0-eed927dbe26c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192648(v=office.15)
ms:contentKeyID: 48544265
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm174420
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c1c8cb8d0f1166b63031925a02186ebc8a1bdac2
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996712"
---
# <a name="minimizewindow-macro-action"></a>MinimizeWindow, action de macro

**S’applique à**: Access 2013, Office 2013

Si Access est configuré pour utiliser des fenêtres superposées au lieu des documents à onglets, vous pouvez utiliser l’action **Réduirefenêtre** pour réduire la fenêtre active à une barre de titre en bas de la fenêtre Access.

> [!NOTE]
> [!REMARQUE] Cette action ne peut être appliquée aux fenêtres de code dans Visual Basic Editor. Pour plus d'informations sur la façon d'affecter des fenêtres de code, reportez-vous à la rubrique relative à la propriété **WindowState**.

## <a name="setting"></a>Valeur

L'action **RéduireFenêtre** ne possède aucun argument.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser cette action pour supprimer une fenêtre de l'écran tout en laissant l'objet ouvert ou pour ouvrir un objet sans afficher sa fenêtre. Pour afficher l'objet, utilisez l'action **SélectionnerObjet** avec l'action **AgrandirFenêtre** ou **RestaurerFenêtre**. L'action **RestaurerFenêtre** rétablit la taille initiale d'une fenêtre réduite.

L'action **RéduireFenêtre** équivaut à cliquer sur le bouton **Réduire** dans le coin supérieur droit de la fenêtre ou à cliquer sur **Réduire** dans le menu **Contrôle** de la fenêtre.

**Conseils**

- Vous devrez peut-être commencer par utiliser la méthode **SélectionnerObjet** si la fenêtre que vous voulez réduire n'est pas la fenêtre active.

- Pour masquer le volet de navigation, utilisez l'action **SélectionnerObjet** avec l'argument DansVoletDeNavigation défini sur **Oui**, puis utilisez l'action **RéduireFenêtre**. L'objet sélectionné dans l'action **SélectionnerObjet** peut être tout objet de la base de données.

- Vous pouvez masquer la fenêtre active en cliquant sur **Gérer cette fenêtre** dans le menu **Affichage**, puis en cliquant sur **Masquer**. Au lieu d'être réduite en icône, la fenêtre devient invisible. Utilisez la commande **Afficher** du même menu pour faire réapparaître la fenêtre. Vous pouvez utiliser l'action **ExécuterCommandeMenu** pour exécuter l'une ou l'autre de ces commandes depuis une macro.

- Vous pouvez également utiliser l'action **DéfinirValeur** pour définir la propriété **Visible** d'un formulaire de manière à masquer ou afficher la fenêtre du formulaire.

Pour exécuter l'action **RéduireFenêtre** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Minimize** de l'objet **DoCmd**.

