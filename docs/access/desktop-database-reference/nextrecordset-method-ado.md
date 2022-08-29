---
title: NextRecordset, méthode (ADO)
TOCTitle: NextRecordset method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 59a2be2315cedbbc87b5140900fad2de791d1b6c
ms.sourcegitcommit: 7c1e7389b18d4f067a69b992ac6c876b5e0441b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2022
ms.locfileid: "67365711"
---
# <a name="nextrecordset-method-ado"></a>NextRecordset, méthode (ADO)

**S’applique à** : Access 2013, Office 2013
 
Efface l’objet [Recordset](recordset-object-ado.md) actif et retourne l’objet **Recordset** suivant en exécutant une série de commandes.

## <a name="syntax"></a>Syntaxe

Définissez *recordset2* = *recordset1*. NextRecordset(*RecordsAffected* )

## <a name="return-value"></a>Valeur renvoyée

Retourne un objet **Recordset**. Dans le modèle de syntaxe, *JeuEnregistrements1* et *JeuEnregistrements2* peuvent représenter le même objet **Recordset** ou vous pouvez utiliser des objets distincts. Lorsque vous utilisez des objets **Recordset** distincts et que vous réinitialisez la propriété **ActiveConnection** sur l'objet **Recordset** d'origine (*JeuEnregistrements1*) après l'appel de **NextRecordset**, une erreur se produit.

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*RecordsAffected* |Facultatif. Variable de type **Long** dans laquelle le fournisseur retourne le nombre d'enregistrements concernés par l'opération actuelle.|

> [!NOTE]
> Ce paramètre ne retourne que le nombre d'enregistrements concernés par une opération ; il ne retourne pas le décompte d'enregistrements d'une instruction Select utilisée pour générer l'objet **Recordset**.

## <a name="remarks"></a>Remarques

Utilisez la méthode **NextRecordset** pour retourner les résultats de la commande suivante dans une instruction de commandes composée ou les résultats d’une procédure stockée qui retourne plusieurs résultats. Si vous ouvrez un objet **Recordset** basé sur une instruction de commande composée (par exemple, « SELECT \* FROM table1 ; SELECT \* FROM table2 « ) à l’aide de la méthode [Execute](/office/vba/access/concepts/miscellaneous/execute-method-ado-command) sur une [commande](command-object-ado.md) ou de la méthode [Open](open-method-ado-recordset.md) sur un **recordset**, ADO exécute uniquement la première commande et retourne les résultats à *l’ensemble d’enregistrements*. Pour accéder aux résultats des commandes suivantes de l'instruction, appelez la méthode **NextRecordset**.

Tant qu’il y a des résultats supplémentaires et que le jeu **d’enregistrements** contenant les instructions composées n’est pas déconnecté ou marshalé au-delà des limites du processus, la méthode **NextRecordset** continue de retourner des objets **Recordset** . Si une commande de renvoi de ligne s’exécute correctement mais ne retourne aucun enregistrement, l’objet **Recordset** retourné est ouvert, mais vide. Testez ce cas en vérifiant que les propriétés [BOF](bof-eof-properties-ado.md) et [EOF](bof-eof-properties-ado.md) sont à la fois **True**. Si une commande ne retournant pas de ligne s’exécute correctement, l’objet **Recordset** retourné est fermé, ce que vous pouvez vérifier en testant la propriété [State](state-property-ado.md) sur **l’objet Recordset**. Lorsqu’il n’y a plus de résultats, *l’ensemble d’enregistrements* est défini sur *Nothing*.

La méthode **NextRecordset** n’est pas disponible sur un objet **Recordset** déconnecté, dont la propriété [ActiveConnection](activeconnection-property-ado.md) a la valeur **Nothing** (en Microsoft Visual Basic) ou NULL (dans les autres langages).

Si une modification est en cours en mode de mise à jour immédiate, l’appel de la méthode **NextRecordset** génère une erreur ; il faut d’abord appeler la méthode [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md).

Pour passer des paramètres à plusieurs commandes dans l'instruction composée en complétant la collection [Parameters](parameters-collection-ado.md) ou en passant un tableau avec l'appel de **Open** ou **Execute** d'origine, les paramètres de la collection ou du tableau doivent respecter le même ordre que leurs commandes correspondantes dans la série de commandes. Vous devez terminer la lecture de tous les résultats avant de lire les valeurs des paramètres de sortie.

Votre fournisseur OLE DB détermine le moment où chaque commande d'une instruction composée est exécutée. Le [fournisseur Microsoft OLE DB pour SQL Server](microsoft-ole-db-provider-for-sql-server.md), par exemple, exécute toutes les commandes dans un lot lorsqu'il reçoit l'instruction composée. Les objets **Recordset** résultants sont simplement retournés lorsque vous appelez **NextRecordset**.

En revanche, il est possible que d'autres fournisseurs n'exécutent la commande suivante d'une instruction qu'après l'appel de NextRecordset. Pour ces fournisseurs, si vous fermez explicitement l'objet **Recordset** avant d'exécuter toute l'instruction, commande par commande, ADO n'exécute jamais les commandes restantes.

