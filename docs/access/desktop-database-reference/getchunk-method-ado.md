---
title: GetChunk, méthode (ADO)
TOCTitle: GetChunk Method (ADO)
ms:assetid: 1ef1c37a-8453-8d3b-251a-d16e0d519fd7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248979(v=office.15)
ms:contentKeyID: 48543629
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6c69ed0363f46f918373cbf5fe141bbbbdb027ef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472241"
---
# <a name="getchunk-method-ado"></a>GetChunk, méthode (ADO)


**S’applique à**: Access 2013 | Office 2013


Retourne l'ensemble ou une partie du contenu d'un objet [Field](field-object-ado.md) volumineux contenant du texte ou des données binaires.

## <a name="syntax"></a>Syntaxe

*variable* = *champ*. GetChunk (*taille* )

## <a name="return-value"></a>Valeur de retour

Retourne une valeur de type **Variant**.

## <a name="parameters"></a>Paramètres

  - *Taille*

  - Expression de type **Long** égale au nombre d'octets ou de caractères que vous souhaitez récupérer.

## <a name="remarks"></a>Notes

Utilisez la méthode **GetChunk** sur un objet **Field** pour récupérer une partie ou l'ensemble de ses données binaires ou de caractères de type long. Dans les cas où la mémoire système est limitée, vous pouvez utiliser la méthode **GetChunk** pour manipuler des parties de données de type long par partie au lieu de l'intégralité de ces données.

Les données renvoyées par une invocation **GetChunk** sont affectées à *variable*. Si la *taille* est supérieure aux données restantes, la méthode **GetChunk** renvoie uniquement les données restantes sans compléter les *variables* avec des espaces vides. Si le champ est vide, la méthode **GetChunk** renvoie une valeur nulle.

Chaque appel à **GetChunk** ultérieur récupère les données à partir de l'emplacement où l'appel à **GetChunk** précédent s'est arrêté. Toutefois, si vous récupérez des données d'un champ et qu'ensuite vous définissez ou lisez la valeur d'un autre champ dans l'enregistrement actif, ADO suppose que vous avez terminé de récupérer les données du premier champ. Si vous appelez de nouveau la méthode **GetChunk** sur le premier champ, ADO interprète l'appel comme une nouvelle opération **GetChunk** et recommence sa lecture à partir du début des données. L'accès à d'autres champs d'objets [Recordset](recordset-object-ado.md) qui ne sont pas des clones du premier objet **Recordset** ne perturbent pas les opérations **GetChunk**.

Si le bit **adFldLong** de la propriété [Attributes](attributes-property-ado.md) d'un objet **Field** a la valeur **True**, vous pouvez utiliser la méthode **GetChunk** pour ce champ.

S'il n'existe aucun enregistrement actif lorsque vous utilisez la méthode **GetChunk** sur un objet **Field**, l'erreur 3021 (aucun enregistrement en cours) se produit.


> [!NOTE]
> <P>[!REMARQUE] La méthode <STRONG>GetChunk</STRONG> ne fonctionne pas sur les objets <STRONG>Field</STRONG> d'un objet <A href="record-object-ado.md">Record</A>. Elle n'exécute aucune opération et génère une erreur d'exécution.</P>


