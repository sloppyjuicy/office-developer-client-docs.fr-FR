---
title: FindNextRecord, action de macro
TOCTitle: FindNextRecord macro action
ms:assetid: 57fb6457-9098-4e81-c693-78ccd262ce0b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194307(v=office.15)
ms:contentKeyID: 48544985
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm89832
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c92a43ce2f4417fde83a544022a90cfca572bf60
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705804"
---
# <a name="findnextrecord-macro-action"></a>FindNextRecord, action de macro


**S’applique à**: Access 2013, Office 2013

Utilisez l'action **RechercherEnregistrementSuivant** pour trouver l'enregistrement suivant qui répond aux critères spécifiés par l'action **TrouverEnregistrement** précédente ou par la valeur de la boîte de dialogue **Rechercher et remplacer** (sous l'onglet **Accueil**, cliquez sur **Rechercher**). Vous pouvez également utiliser l'action **RechercherEnregistrementSuivant** pour rechercher un à un des enregistrements, par exemple des enregistrements relatifs à un client spécifique.

## <a name="setting"></a>Valeur

L’action **Rechercherenregistrementsuivant** ne possède aucun argument. L’action **Rechercherenregistrementsuivant** recherche l’enregistrement suivant qui répond aux critères définis par l’action **TrouverEnregistrement** ou dans la boîte de dialogue **Rechercher et remplacer** . Les arguments de l’action **TrouverEnregistrement** sont partagés avec les options dans la boîte de dialogue **Rechercher et remplacer** .

Pour définir les critères de recherche, utilisez l'action **TrouverEnregistrement**. Généralement, vous entrez une action **TrouverEnregistrement** dans une macro, puis utilisez l'action **RechercherEnregistrementSuivant** pour rechercher un à un les enregistrements répondant aux mêmes critères. Pour rechercher des enregistrements uniquement lorsqu'une certaine condition est remplie, vous pouvez entrer une expression conditionnelle dans la colonne **Condition** de la ligne correspondant à l'action **RechercherEnregistrementSuivant**.

## <a name="remarks"></a>Remarques

Cette action équivaut à utiliser le bouton **Suivant** dans la boîte de dialogue **Rechercher et remplacer**.

> [!NOTE]
> [!REMARQUE] Bien que l'action **TrouverEnregistrement** corresponde à la commande **Rechercher** de l'onglet **Accueil** pour les tables, requêtes et formulaires, elle ne correspond pas à la commande **Rechercher** du menu **Edition** dans la fenêtre Code. Vous ne pouvez pas utiliser l'action **TrouverEnregistrement** ni l'action **RechercherEnregistrementSuivant** pour rechercher du texte dans des modules.

> [!TIP]
> [!CONSEIL] Si vous avez défini l'argument **Champ actif uniquement** de l'action **TrouverEnregistrement** sur **Oui**, vous devrez peut-être utiliser l'action **AtteindreContrôle** pour déplacer le focus sur le contrôle contenant les données que vous recherchez avant d'utiliser l'action **RechercherEnregistrementSuivant**.

Si le texte actuellement sélectionné correspond au texte recherché au moment de l'exécution de l'action de macro **RechercherEnregistrementSuivant**, la recherche commence immédiatement après la sélection, dans le même champ que la sélection et dans le même enregistrement. Sinon, la recherche commence au début de l'enregistrement actif. Cela vous permet de rechercher plusieurs instances des mêmes critères de recherche dans un même enregistrement.

Notez toutefois que si vous utilisez un bouton de commande pour exécuter une macro contenant l'action **RechercherEnregistrementSuivant**, la première instance des critères de recherche sera trouvée en boucle. En effet, le fait de cliquer sur le bouton de commande supprime le focus du champ contenant la valeur correspondante. L'action **RechercherEnregistrementSuivant** commencera la recherche au début de l'enregistrement. Pour éviter cela, exécutez la macro à l'aide d'une technique qui ne modifie pas le focus, comme un bouton de barre d'outils personnalisé ou une combinaison de touches définie dans une macro AutoKeys. Vous pouvez également définir le focus dans la macro sur le champ contenant les critères de recherche avant d'exécuter l'action **RechercherEnregistrementSuivant**.

Ce comportement est également observé si vous utilisez un bouton de commande pour exécuter une macro contenant l'action **TrouverEnregistrement** avec l'argument **Trouver le premier** défini sur **Non**.

Pour exécuter l'action **RechercherEnregistrementSuivant** dans un module Visual Basic pour Applications, utilisez la méthode **FindNext** de l'objet **DoCmd**.

