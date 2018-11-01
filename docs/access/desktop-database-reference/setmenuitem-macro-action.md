---
title: DéfinirElémentMenu, action de macro
TOCTitle: SetMenuItem Macro Action
ms:assetid: 503b3635-e721-1b99-3249-626e5dccdb8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193803(v=office.15)
ms:contentKeyID: 48544789
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm16614
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d7a7de3d627dacfa0ca014a80ea037d0728220d1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873564"
---
# <a name="setmenuitem-macro-action"></a>DéfinirElémentMenu, action de macro


**S’applique à**: Access 2013, Office 2013

Vous pouvez utiliser l'action **DéfinirElémentMenu** pour définir l'état des éléments de menu (activé, désactivé, sélectionné ou non sélectionné) dans les menus globaux ou personnalisés de l'onglet **Compléments**.


> [!NOTE]
> <P>[!REMARQUE] L'action <STRONG>DéfinirElémentMenu</STRONG> fonctionne uniquement avec les menus personnalisés et globaux générés à l'aide de macros de menu. L'action <STRONG>DéfinirElémentMenu</STRONG> est incluse dans Microsoft Access à la seule fin de compatibilité avec les versions antérieures. Il ne fonctionne pas avec les fonctionnalités de la barre de commandes. Vous pouvez toutefois utiliser les propriétés <STRONG>Enabled</STRONG> et <STRONG>State</STRONG> dans un module Visual Basic pour Applications (VBA) afin de désactiver, d'activer, de sélectionner ou de désélectionner des éléments des menus contextuels ou des menus personnalisés ou globaux.</P>



## <a name="setting"></a>Valeur

L'action **DéfinirElémentMenu** accepte les arguments suivants.

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
<td><p><strong>Index de menu</strong></p></td>
<td><p>L’index du menu qui contient la commande pour laquelle vous souhaitez définir l’état. Entrez une valeur entière, à partir de 0, pour l’index du menu souhaité dans le menu personnalisé ou global. Dans la zone <strong>Index de Menu</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro, entrez la valeur d’index. L’index est par rapport à la position du menu dans la macro de menu pour le menu personnalisé ou global (position de l’action <strong>AjouterMenu</strong> de ce menu dans la macro de menu, à partir de 0). L’affichage du menu peut être légèrement différent, car vous pouvez utiliser des expressions conditionnelles dans la macro de menu pour masquer ou afficher des éléments de menu personnalisés. Cet argument est obligatoire. Si vous sélectionnez un menu avec cet argument et laissez les arguments <strong>Index de commande</strong> et <strong>Index de sous-commande</strong> vides, vous pouvez activer ou désactiver le nom du menu lui-même. Toutefois, vous ne peut pas sélectionner ou désélectionner un nom de menu (Access ignore les paramètres <strong>coché</strong> et <strong>non coché</strong> de l’argument <strong>indicateur</strong> pour les noms de menu).</p></td>
</tr>
<tr class="even">
<td><p><strong>Index de commande</strong></p></td>
<td><p>Index de la commande dont vous souhaitez définir l’état. Entrez une valeur entière, à partir de 0, pour l’index de la commande souhaitée dans le menu sélectionné par l’argument <strong>Index de menu</strong>. L’index est relatif à la position de la commande dans le groupe de macros qui définit le menu sélectionné pour le menu personnalisé ou global (position de la macro de cette commande dans le groupe de macros, à partir de 0). L’affichage du menu peut être légèrement différent dans la mesure où vous pouvez utiliser des expressions conditionnelles dans le groupe de macros du menu pour masquer ou afficher les commandes de menu personnalisées.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Index de sous-commande</strong></p></td>
<td><p>Index de la sous-commande dont vous souhaitez définir l’état. Cet argument n’est applicable qu’à partir du moment où la commande souhaitée possède un sous-menu. Entrez une valeur entière, à partir de 0, pour l’index de la sous-commande requise dans le sous-menu sélectionné par l’argument <strong>Index de commande</strong>. L’index est relatif à la position de la sous-commande dans le groupe de macros qui définit le sous-menu sélectionné pour le menu personnalisé ou global (position de la macro de cette sous-commande dans le groupe de macros, à partir de 0).</p></td>
</tr>
<tr class="even">
<td><p><strong>Flag</strong></p></td>
<td><p>État à affecter à la commande ou à la sous-commande. Cliquez sur <strong>Grisé</strong> (pour désactiver la commande qui apparaît estompée), <strong>Non grisé</strong> (pour l’activer), <strong>Coché</strong> (pour placer une coche en regard de la commande, ce qui indique en général qu’elle a été sélectionnée) ou <strong>Non coché</strong> (pour supprimer la coche). La valeur par défaut est <strong>Non grisé</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

L'action **DéfinirElémentMenu** fonctionne uniquement avec un menu personnalisé ou global. Si la fenêtre active ne possède pas de menu personnalisé ou global, l'exécution d'une macro contenant l'action **DéfinirElémentMenu** provoque une erreur d'exécution.

Vous pouvez utiliser cette action pour définir l'état des commandes et sous-commandes de menu, mais non des sous-commandes de sous-commandes.

Pour exécuter l'action **DéfinirÉlémentMenu** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **SetMenuItem** de l'objet **DoCmd**.

