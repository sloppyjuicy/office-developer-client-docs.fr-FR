---
title: Find, méthode - ActiveX Data Objects (ADO)
TOCTitle: Find Method (ADO)
ms:assetid: a7cc9ceb-fdb9-73e2-8328-70b174f93cda
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249776(v=office.15)
ms:contentKeyID: 48546887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 929e4ac695ff65c3576f2ffb8ad1baf8ab1d1137
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870624"
---
# <a name="find-method-ado"></a>Find, méthode (ADO)


**S’applique à**: Access 2013, Office 2013


Recherche un objet [Recordset](recordset-object-ado.md) pour la ligne qui répond aux critères spécifiés. Il est éventuellement possible de spécifier des paramètres facultatifs, tels que la direction de la recherche, la ligne de début et un décalage par rapport à la ligne de début. Si les critères sont satisfaits, la position de ligne actuelle est définie sur l'enregistrement identifié ; sinon la position est définie à la fin (ou au début) de l'objet **Recordset**.

## <a name="syntax"></a>Syntaxe

Rechercher (*critères*, *SkipRows*, *SearchDirection*, *Démarrer*)

## <a name="parameters"></a>Paramètres

  - *Critères*

  - Une valeur de type **String** qui contient une instruction spécifiant le nom de colonne, l'opérateur de comparaison et la valeur à utiliser dans la recherche.

  - *SkipRows*

  - Facultatif *.* Valeur de type **Long**, dont la valeur par défaut est zéro et qui spécifie le décalage de lignes par rapport à la ligne active ou un signet *Start* à partir duquel commencer la recherche. Par défaut, la recherche commence à partir de la ligne active.

  - *SearchDirection*

  - Facultatif *.* Valeur [SearchDirectionEnum](searchdirectionenum.md) qui spécifie si la recherche doit commencer à partir de la ligne active ou de la ligne disponible suivante selon la direction de la recherche. Une recherche qui ne donne aucun résultat s’arrête à la fin de l’objet **Recordset** si la valeur est **adSearchForward**. En revanche, elle s’arrête au début de l’objet **Recordset** si la valeur est **adSearchBackward**.

  - *Début*

  - Facultatif. Signet de type **Variant** qui indique la position de début de la recherche.

## <a name="remarks"></a>Notes

Un seul nom de colonne peut être spécifié dans *Critères*. Cette méthode ne prend pas en charge les recherches dans plusieurs colonnes.

L’opérateur de comparaison dans *critères* peut être «**\>**« (supérieur à), »**\<**« (inférieur à), « = » (égal à), »\>= » (supérieur ou égal à), «\<= » (inférieur ou égal à), «\<\>» (différent de), ou « like » (correspondance).

La valeur de *critères* peut être une chaîne, un nombre à virgule flottante ou une date. Valeurs de chaîne sont délimitées par des guillemets simples ou «\#» (signe dièse) marque (par exemple, « état = 'WA' » ou « état = \#WA\#»). Valeurs de date sont délimitées par des «\#» (signe dièse) marque (par exemple, « démarrer\_date \> \#7/22/97\#») et peuvent contenir des heures, minutes et secondes pour indiquer l’horodatage mais ne doivent pas contenir de millisecondes ou erreurs seront produit .

Si l'opérateur de comparaison est « like », la valeur de chaîne peut contenir un astérisque (\*) pour rechercher une ou plusieurs occurrences d'un caractère ou sous-chaîne. Par exemple, « state like 'M\*' »" correspond aux états du Maine et du Massachusetts. Vous pouvez également utiliser des astérisques de début ou de fin pour rechercher une sous-chaîne contenue dans les valeurs. Par exemple, « state like '\*as\*' »" correspond aux états de l'Alaska, de l'Arkansas et du Massachusetts.

Les astérisques peuvent uniquement être utilisés à la fin d'une chaîne de critères ou au début et à la fin de celle-ci, comme illustré ci-dessus. Vous ne pouvez pas l'employer comme caractère générique de début ('\*str') ou incorporé ('s\*r'). Cela provoque une erreur.


> [!NOTE]
> <P>[!REMARQUE] Une erreur se produit si la position de ligne actuelle n'est pas définie avant d'appeler <STRONG>Find</STRONG>. Toute méthode qui définit la position de ligne, par exemple <A href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</A>, doit être appelée avant la méthode <STRONG>Find</STRONG>.</P>




> [!NOTE]
> <P>[!REMARQUE] Si vous appelez la méthode <STRONG>Find</STRONG> sur un jeu d'enregistrements et que la position actuelle dans le jeu d'enregistrements correspond au dernier enregistrement ou à la fin du fichier (EOF), votre recherche ne donne aucun résultat. Vous devez appeler la méthode <STRONG>MoveFirst</STRONG> pour définir la position/le curseur actuel au début du jeu d'enregistrements.</P>


