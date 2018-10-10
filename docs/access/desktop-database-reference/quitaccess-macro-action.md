---
title: QuitterAccess, action de macro
TOCTitle: QuitAccess Macro Action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5fa3b7ffc97f69b1ebc85799a8b2a27b6acc1d90
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469263"
---
# <a name="quitaccess-macro-action"></a>QuitterAccess, action de macro


**S’applique à**: Access 2013 | Office 2013

Vous pouvez utiliser l'action **QuitterAccess** pour quitter Microsoft Access. L'action **QuitterAccess** peut également spécifier une des options d'enregistrement d'objets de base de données avant de quitter Access.


> [!NOTE]
> <P>[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</P>



## <a name="setting"></a>Paramètre

L'action **QuitterAccess** utilise l'argument suivant :

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
<td><p><strong>Options</strong></p></td>
<td><p>Spécifie l’action appliquée aux objets non enregistrés lorsque vous quittez Access. Cliquez sur <strong>Avec confirmation</strong> (pour afficher des boîtes de dialogue qui vous demandent si vous souhaitez enregistrer chaque objet), sur <strong>Enregistrer tout</strong> (pour enregistrer tous les objets sans demander de confirmation) ou sur <strong>Quitter</strong> (pour quitter sans enregistrer d’objet) dans la zone <strong>Options</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. La valeur par défaut est <strong>Enregistrer tout</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Access n'exécute aucune action après l'action **QuitterAccess** dans une macro.

Cette action vous permet de quitter Access sans afficher de demande de confirmation dans les boîtes de dialogue **Enregistrer** en utilisant une commande de menu personnalisée ou un bouton dans un formulaire. Vous pouvez, par exemple, avoir un formulaire de base que vous utilisez pour afficher des objets dans votre espace de travail personnalisé. Ce formulaire peut comporter un bouton **Quitter** qui exécute une macro contenant l'action **QuitterAccess** avec la valeur **Enregistrer tout** définie pour l'argument **Options**.

Cette action équivaut à cliquer sur l'onglet **Fichier**, puis sur **Quitter**. Si des objets ne sont pas encore enregistrés lorsque vous cliquez sur cette commande, les boîtes de dialogue qui s'affichent sont identiques à celles qui apparaissent lorsque vous sélectionnez la valeur **Demander** pour l'argument **Options** de l'action **QuitterAccess**.

Vous pouvez utiliser l'action **EnregistrerObjet** d'une macro pour enregistrer un objet spécifié sans devoir quitter Access ou fermer l'objet.

Pour exécuter l'action **QuitterAccess** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Quit** de l'objet **DoCmd**.

