---
title: FindRecord, action de macro
TOCTitle: FindRecord macro action
ms:assetid: 379e3dda-cb7d-a294-29b1-c6ce9a62ba8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192494(v=office.15)
ms:contentKeyID: 48544199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm7496
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 19b6c80af2bcee9ca3dbe51bbbcf56343f33d550
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937609"
---
# <a name="findrecord-macro-action"></a>FindRecord, action de macro

**S’applique à**: Access 2013, Office 2013

Vous pouvez utiliser l’action **TrouverEnregistrement** pour rechercher la première instance de données qui répondent aux critères spécifiés par les arguments **TrouverEnregistrement** . Ces données peuvent être dans l’enregistrement actif, dans un enregistrement suivant ou précédent ou dans le premier enregistrement. Vous pouvez rechercher des enregistrements dans la table active feuille de données, requête, formulaire ou formulaire.

## <a name="setting"></a>Valeur

L'action **TrouverEnregistrement** possède les arguments suivants.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Rechercher</strong></p></td>
<td><p>Spécifie les données que vous souhaitez rechercher dans l’enregistrement. Entrez le texte, nombre ou date que vous souhaitez rechercher ou tapez une expression précédée d’un signe égal (<strong>=</strong>), dans la zone <strong>Rechercher</strong> , dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro. Vous pouvez utiliser des caractères génériques. Cet argument est obligatoire.</p></td>
</tr>
<tr class="even">
<td><p><strong>Match</strong></p></td>
<td><p>Spécifie où se trouvent les données dans le champ. Vous pouvez rechercher des données dans toute partie du champ (<strong>N’importe où dans le champ</strong>), des données qui remplissent tout le champ (<strong>Champ entier</strong>) ou des données situées au début du champ (<strong>Début de champ</strong>). La valeur par défaut est <strong>Champ entier</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Respecter la casse</strong></p></td>
<td><p>Indique si la recherche respecte la casse. Cliquez sur <strong>Oui</strong> (effectuer une recherche qui respecte la casse) ou sur <strong>Non</strong> (effectuer la recherche sans respecter les majuscules et les minuscules). La valeur par défaut est <strong>Non</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Rechercher</strong></p></td>
<td><p>Spécifie si la recherche part de l’enregistrement actif et remonte jusqu’au début des enregistrements (<strong>Haut</strong>), descend jusqu’à la fin des enregistrements (<strong>Bas</strong>) ou descend jusqu’à la fin des enregistrements, puis repart du début des enregistrements jusqu’à l’enregistrement actif afin que tous les enregistrements soient inclus dans la recherche (<strong>Tous</strong>). La valeur par défaut est <strong>Tous</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Avec mise en forme</strong></p></td>
<td><p>Spécifie si la recherche inclut les données mises en forme. Cliquez sur <strong>Oui</strong> (Microsoft Office Access 2007 recherche les données qu’il est mis en forme et affiché dans le champ) ou sur <strong>non</strong> (Access recherche les données qu’il est stocké dans la base de données, ce qui n’est pas toujours les mêmes tel qu’il est affiché). La valeur par défaut est <strong>Non</strong>. Vous pouvez utiliser cette fonctionnalité pour limiter la recherche à des données dans un format particulier. Par exemple, cliquez sur <strong>Oui</strong> , tapez <strong>1 234</strong> dans l’argument <strong>Rechercher</strong> pour trouver la valeur 1 234 dans un champ formaté afin d’inclure des virgules. Cliquez sur <strong>non</strong> si vous souhaitez entrer <strong>1234</strong> pour rechercher des données dans ce champ. Pour rechercher des dates, cliquez sur <strong>Oui</strong> pour rechercher une date exactement comme elle est formatée, comme 08-juillet-2003. Si vous cliquez sur <strong>non</strong>, entrez la date pour l’argument <strong>Rechercher</strong> dans le format défini dans les paramètres régionaux du Panneau de configuration Windows. Ce format est indiqué dans la zone <strong>format de date court</strong> de l’onglet <strong>Date</strong> dans les paramètres régionaux. Par exemple, si la zone <strong>format de date court</strong> est définie sur <strong>jj/aa</strong>, vous pouvez entrer 7/8/03, et Access trouve toutes les entrées dans un champ Date correspondant au 8 juillet 2003, quelle que soit la façon dont ce champ est mis en forme.</p>

> [!NOTE]
> L’argument **Avec mise en forme** est appliqué uniquement si le champ actif est un contrôle dépendant, si l’argument **Où** est défini sur **Champ entier**, si l’argument **Champ actif uniquement** est défini sur **Oui** et si l’argument **Respecter la casse** est défini sur **Non**.


<p>Si vous définissez <strong>Respecter la casse</strong> sur <strong>Oui</strong> ou <strong>Champ actif uniquement</strong> sur <strong>Non</strong>, vous devez également définir <strong>Avec mise en forme</strong> sur <strong>Oui</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Champ actif uniquement</strong></p></td>
<td><p>Spécifie si la recherche est limitée au champ actif de chaque enregistrement ou si elle inclut tous les champs de chaque enregistrement. La recherche dans le champ actif est plus rapide. Cliquez sur <strong>Oui</strong> (limiter la recherche au champ actif) ou sur <strong>Non</strong> (rechercher dans tous les champs de chaque enregistrement). La valeur par défaut est <strong>Oui</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Trouver le premier</strong></p></td>
<td><p>Indique si la recherche débute au premier enregistrement ou à l’enregistrement actif. Cliquez sur <strong>Oui</strong> (démarrer au premier enregistrement) ou sur <strong>Non</strong> (démarrer à l’enregistrement actif). La valeur par défaut est <strong>Oui</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Lorsqu'une macro exécute l'action **TrouverEnregistrement**, Access recherche les données spécifiées dans les enregistrements (l'ordre de la recherche est déterminé par le paramètre de l'argument **Sens** ). Lorsqu'Access trouve les données spécifiées, elles sont sélectionnées dans l'enregistrement.

L'action **TrouverEnregistrement** équivaut à cliquer sur **Rechercher** sous l'onglet **Accueil** et ses arguments sont identiques aux options de la boîte de dialogue **Rechercher et remplacer**. Si vous définissez les arguments de l'action **TrouverEnregistrement** dans le volet Générateur de macro, puis exécutez la macro, les options correspondantes sont sélectionnées dans la boîte de dialogue **Rechercher et remplacer** lorsque vous cliquez sur **Rechercher**.

Access conserve les arguments les plus récents de l'action **TrouverEnregistrement** au cours d'une session de base de données afin que vous n'ayez pas à réentrer les mêmes critères si vous utilisez plusieurs fois l'action **TrouverEnregistrement**. Si vous laissez un argument vide, Access utilise le paramètre le plus récent de cet argument, qu'il ait été défini par une action **TrouverEnregistrement** précédente ou dans la boîte de dialogue **Rechercher et remplacer**.

Si vous souhaitez rechercher un enregistrement à l'aide d'une macro, utilisez l'action **TrouverEnregistrement**, et non l'action **ExécuterCommandeMenu** avec ses arguments définis pour exécuter la commande **Rechercher**.

> [!NOTE]
> [!REMARQUE] Bien que l'action **TrouverEnregistrement** corresponde à la commande **Rechercher** sous l'onglet **Accueil** pour les tables, les requêtes et les formulaires, elle ne correspond pas à la commande **Rechercher** dans le menu **Edition** de la fenêtre Code. Vous ne pouvez pas utiliser l'action **TrouverEnregistrement** pour rechercher du texte dans les modules.

Si le texte actuellement sélectionné correspond au texte recherché au moment de l'exécution de l'action **TrouverEnregistrement**, la recherche commence immédiatement après la sélection, dans le même champ que la sélection et dans le même enregistrement. Sinon, la recherche commence au début de l'enregistrement actif. Cela vous permet de rechercher plusieurs instances des mêmes critères de recherche dans un même enregistrement.

Notez toutefois que si vous utilisez un bouton de commande pour exécuter une macro contenant l'action **TrouverEnregistrement**, la première instance des critères de recherche sera trouvée en boucle. En effet, le fait de cliquer sur le bouton de commande supprime le focus du champ contenant la valeur correspondante. L'action **TrouverEnregistrement** commencera la recherche au début de l'enregistrement. Pour éviter cela, exécutez la macro à l'aide d'une technique qui ne modifie pas le focus, comme un bouton de barre d'outils personnalisé ou une combinaison de touches définie dans une macro AutoKeys. Vous pouvez également définir le focus dans la macro sur le champ contenant les critères de recherche avant d'exécuter l'action **TrouverEnregistrement**.

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Remarque sur la sécurité" alt="Security note" />de sécurité**</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>
      Évitez d’utiliser l’instruction <strong>SendKeys</strong> ou une macro AutoKeys avec des informations sensibles et confidentielles. Un utilisateur malveillant pourrait intercepter la frappe et compromettre la sécurité de votre ordinateur et de vos données.
</td>
</tr>
</tbody>
</table>

Ce comportement est également observé si vous utilisez un bouton de commande pour exécuter une macro contenant l'action **TrouverSuivant**.

Pour exécuter l'action **TrouverEnregistrement** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **FindRecord** de l'objet **DoCmd**.

Pour les recherches plus complexes, vous voudrez peut-être utiliser l'action de macro **RechercherEnregistrement**.

