---
title: Boîte de dialogue des propriétés personnalisées du contrôle ActiveX
TOCTitle: ActiveX Control's Custom Properties Dialog Box
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6f5924d04e9ea4febee1434f6ef99f95b02eab6b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471091"
---
# <a name="activex-controls-custom-properties-dialog-box"></a>Boîte de dialogue des propriétés personnalisées du contrôle ActiveX

**S’applique à**: Access 2013 | Office 2013

Lors de la définition des propriétés d'un contrôle ActiveX, vous devrez ou souhaiterez peut-être utiliser la boîte de dialogue des propriétés personnalisée du contrôle. Cette boîte de dialogue des propriétés personnalisée propose une alternative à la liste des propriétés figurant dans la feuille des propriétés Microsoft Access pour définir les propriétés d'un contrôle ActiveX en mode Création de formulaire.

> [!NOTE]
> [!REMARQUE] Ces informations s'appliquent uniquement aux contrôles ActiveX dans un environnement de base de données Microsoft Access.



## <a name="two-ways-to-set-properties"></a>Deux manières de définir des propriétés

La raison d'être de la boîte de dialogue des propriétés personnalisée est que toutes les applications qui utilisent des contrôles ActiveX ne fournissent pas une feuille des propriétés comme Microsoft Access. La boîte de dialogue des propriétés personnalisée fournit une interface pour la définition des propriétés clés du contrôle sans tenir compte de l'interface fournie par l'application hôte.

Pour certaines propriétés de contrôle ActiveX, vous pouvez choisir un des deux endroits suivants pour définir la propriété :

  - La feuille des propriétés Microsoft Access.

  - La boîte de dialogue des propriétés personnalisée du contrôle ActiveX.

Dans certains cas, la boîte de dialogue des propriétés personnalisée est la seule manière de définir une propriété en mode Création. Cela est généralement le cas lorsque l'interface nécessaire pour définir une propriété ne fonctionne pas avec la feuille des propriétés de Microsoft Access. Par exemple, la propriété **GridFont** du contrôle Calendrier dispose d'un certain nombre d'éléments, mais vous ne pouvez en définir qu'un seul par propriété à l'aide de la feuille des propriétés de Microsoft Access.

## <a name="finding-the-custom-properties-dialog-box"></a>Recherche de la boîte de dialogue des propriétés personnalisée

Tous les contrôles ActiveX ne fournissent pas une boîte de dialogue des propriétés personnalisée. Pour voir si un contrôle fournit cette boîte de dialogue des propriétés personnalisée, recherchez la propriété **Personnalisé** de ce contrôle dans la feuille des propriétés de Microsoft Access. Si la liste des propriétés contient le nom **Personnalisé**, cela signifie que le contrôle fournit la boîte de dialogue des propriétés personnalisée.

## <a name="using-the-custom-properties-dialog-box"></a>Utilisation de la boîte de dialogue des propriétés personnalisée

Après avoir cliqué dans la zone de propriété **Personnalisé** de la feuille des propriétés de Microsoft Access, cliquez sur le bouton **Générer** à droite de la zone des propriétés pour afficher la boîte de dialogue des propriétés personnalisée du contrôle, qui apparaît souvent sous la forme d'une boîte de dialogue comportant des onglets. Choisissez l'onglet contenant l'interface permettant de définir les propriétés souhaitées.

Le plus souvent, après avoir effectué les changements dans un onglet, vous pouvez les appliquer immédiatement en cliquant sur le bouton **Appliquer** (s'il est fourni). Vous pouvez cliquer sur les autres onglets pour définir les autres propriétés. Pour approuver tous les changements effectués dans la boîte de dialogue des propriétés personnalisée, cliquez sur le bouton **OK**. Pour retourner à la feuille des propriétés de Microsoft Access sans modification, cliquez sur le bouton **Annuler**.

Vous pouvez afficher la boîte de dialogue des propriétés personnalisée en cliquant sur la sous-commande **Propriétés** de la commande **Objet** du contrôle ActiveX (par exemple, **Contrôle Calendrier**) dans le menu **Edition** ou en cliquant sur la même sous-commande du menu contextuel du contrôle ActiveX. De plus, certaines propriétés dans la feuille des propriétés de Microsoft Access du contrôle ActiveX, comme la propriété **GridFontColor** du contrôle Calendrier, disposent d'un bouton **Générer** à droite de la zone des propriétés. Lorsque vous cliquez sur le bouton **Générer**, la boîte de dialogue des propriétés personnalisée s'affiche avec les onglets appropriés sélectionnés (par exemple, l'onglet **Couleurs**).

