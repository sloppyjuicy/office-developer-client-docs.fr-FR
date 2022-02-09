---
title: Masquer le ruban au démarrage d’Access
TOCTitle: Hide the ribbon when Access starts
description: Comment charger un ruban personnalisé qui masque tous les onglets prédéfinis dans Access 2013.
ms:assetid: f98bab58-8094-1c56-f70b-ced2e7849574
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837012(v=office.15)
ms:contentKeyID: 48548817
ms.date: 10/16/2018
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: b2163e448808c6e23416dac15a18f017997e00b2
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462602"
---
# <a name="hide-the-ribbon-when-access-starts"></a>Masquer le ruban au démarrage d’Access

**S’applique à** : Access 2013 | Office 2013

Par défaut, Microsoft Access ne fournit pas de méthode pour masquer le ruban. Cette rubrique décrit comment charger un ruban personnalisé qui masque tous les onglets prédéfinis.

Pour charger le ruban personnalisé au démarrage d'Access, vous devez stocker ses paramètres dans une table dénommée **RubansSysU**.

Cette **table** doit être créée en utilisant des noms de colonnes spécifiques afin que les personnalisations du ruban soient implémentées. 

Le tableau suivant répertorie les paramètres à utiliser lors de la création du tableau **USysRibbons**.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom de colonne</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>RibbonName</strong></p></td>
<td><p>Text</p></td>
<td><p>Contient le nom du ruban personnalisé devant être associé à cette personnalisation.</p></td>
</tr>
<tr class="even">
<td><p><strong>RibbonXML</strong></p></td>
<td><p>Mémo</p></td>
<td><p>Contient le XML d'extensibilité du ruban (RibbonX) qui définit la personnalisation du ruban.</p></td>
</tr>
</tbody>
</table>


Le tableau suivant répertorie les paramètres de personnalisation du ruban pour les stocker dans le tableau **USysRibbons**.

|Nom de colonne|Valeur|
|:----------|:----|
|**RibbonName**|HideTheRibbon|
|**RibbonXML**|`<CustomUI xmlns="http://schemas.microsoft.com/office/2006/01/CustomUI"> <ribbon startFromScratch="true"/></CustomUI>`|


## <a name="apply-a-custom-ribbon-when-access-starts"></a>Appliquer un ruban personnalisé au démarrage d’Access

Pour appliquer un ruban personnalisé disponible au démarrage de l'application, procédez comme suit :

1.  Suivez le processus décrit précédemment pour rendre le ruban personnalisé disponible pour cette application.

2.  Redémarrez l'application.

3.  Choisissez le **Microsoft Office bouton**![O12FileMenuButton \_ ZA10077102,](media/access-file-menu-button.gif "O12FileMenuButton_ZA10077102")puis choisissez **Options Access.**

4.  Cliquez sur l'option **Base de données active**, dans la section **Options de la barre d'outils et du ruban**, puis sur la liste **Nom du ruban** et sélectionnez **MasquerLeRuban**.

5.  Fermez er redémarrez l'application.

> [!NOTE]
> Pour plus d'informations sur l'interface du ruban dans d'autres applications Office, consultez l'article [Vue d'ensemble du ruban Office Fluent](https://docs.microsoft.com/office/vba/Library-Reference/Concepts/overview-of-the-office-fluent-ribbon).


