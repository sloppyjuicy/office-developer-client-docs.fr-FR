---
title: NextRecordset, méthode (ADO)
TOCTitle: NextRecordset Method (ADO)
ms:assetid: d2776dd5-d521-c57f-dbe5-e02ee238104d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250051(v=office.15)
ms:contentKeyID: 48547887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b824dc1b00f913e097432aae65ecac425ef19031
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472373"
---
# <a name="nextrecordset-method-ado"></a><span data-ttu-id="ea6a3-102">NextRecordset, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="ea6a3-102">NextRecordset Method (ADO)</span></span>


<span data-ttu-id="ea6a3-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ea6a3-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="ea6a3-104">Efface l'objet [Recordset](recordset-object-ado.md) actif et retourne l'objet **Recordset** suivant en exécutant une série de commandes.</span><span class="sxs-lookup"><span data-stu-id="ea6a3-104">Clears the current [Recordset](recordset-object-ado.md) object and returns the next **Recordset** by advancing through a series of commands.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea6a3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea6a3-105">Syntax</span></span>

<span data-ttu-id="ea6a3-106">Définir *l’objet recordset2* = *recordset1*. NextRecordset (*RecordsAffected* )</span><span class="sxs-lookup"><span data-stu-id="ea6a3-106">Set *recordset2* = *recordset1*.NextRecordset(*RecordsAffected* )</span></span>

## <a name="return-value"></a><span data-ttu-id="ea6a3-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ea6a3-107">Return Value</span></span>

<span data-ttu-id="ea6a3-p101">Retourne un objet **Recordset**. Dans le modèle de syntaxe, *JeuEnregistrements1* et *JeuEnregistrements2* peuvent représenter le même objet **Recordset** ou vous pouvez utiliser des objets distincts. Lorsque vous utilisez des objets **Recordset** distincts et que vous réinitialisez la propriété **ActiveConnection** sur l'objet **Recordset** d'origine (*JeuEnregistrements1*) après l'appel de **NextRecordset**, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="ea6a3-p101">Returns a **Recordset** object. In the syntax model, *recordset1* and *recordset2* can be the same **Recordset** object, or you can use separate objects. When using separate **Recordset** objects, resetting the **ActiveConnection** property on the original **Recordset** (*recordset1*) after **NextRecordset** has been called will generate an error.</span></span>

## <a name="parameters"></a><span data-ttu-id="ea6a3-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea6a3-111">Parameters</span></span>

- <span data-ttu-id="ea6a3-112">*RecordsAffected*</span><span class="sxs-lookup"><span data-stu-id="ea6a3-112">*RecordsAffected*</span></span>

- <span data-ttu-id="ea6a3-p102">Facultatif. Variable de type **Long** dans laquelle le fournisseur retourne le nombre d'enregistrements concernés par l'opération actuelle.</span><span class="sxs-lookup"><span data-stu-id="ea6a3-p102">Optional. A **Long** variable to which the provider returns the number of records that the current operation affected.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ea6a3-115">[!REMARQUE] Ce paramètre ne retourne que le nombre d'enregistrements concernés par une opération ; il ne retourne pas le décompte d'enregistrements d'une instruction Select utilisée pour générer l'objet <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="ea6a3-115">This parameter only returns the number of records affected by an operation; it does not return a count of records from a select statement used to generate the <STRONG>Recordset</STRONG>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="ea6a3-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ea6a3-116">Remarks</span></span>

<span data-ttu-id="ea6a3-117">Utilisez la méthode **NextRecordset** pour retourner les résultats de la commande suivante dans une instruction de commandes composée ou les résultats d'une procédure stockée qui retourne plusieurs résultats.</span><span class="sxs-lookup"><span data-stu-id="ea6a3-117">Use the **NextRecordset** method to return the results of the next command in a compound command statement or of a stored procedure that returns multiple results.</span></span> <span data-ttu-id="ea6a3-118">Si vous ouvrez un objet **Recordset** basé sur une instruction de commandes composée (par exemple, « sélectionnez \* FROM table1 ; Sélectionnez \* FROM table2 ») à l’aide de la méthode [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) sur une [commande](command-object-ado.md) ou la méthode [Open](open-method-ado-recordset.md) sur un **objet Recordset**, ADO exécute uniquement la première commande et retourne les résultats à *l’objet recordset*.</span><span class="sxs-lookup"><span data-stu-id="ea6a3-118">If you open a **Recordset** object based on a compound command statement (for example, "SELECT \* FROM table1;SELECT \* FROM table2") using the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method on a [Command](command-object-ado.md) or the [Open](open-method-ado-recordset.md) method on a **Recordset**, ADO executes only the first command and returns the results to *recordset*.</span></span> <span data-ttu-id="ea6a3-119">Pour accéder aux résultats des commandes suivantes de l'instruction, appelez la méthode **NextRecordset**.</span><span class="sxs-lookup"><span data-stu-id="ea6a3-119">To access the results of subsequent commands in the statement, call the **NextRecordset** method.</span></span>

<span data-ttu-id="ea6a3-120">Tant que des résultats supplémentaires sont et l' **objet Recordset** contenant les instructions composées n’est pas déconnecté ni marshalé au-delà des limites du processus, la méthode **NextRecordset** continue de retourner des objets **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="ea6a3-120">As long as there are additional results and the **Recordset** containing the compound statements is not disconnected or marshaled across process boundaries, the **NextRecordset** method will continue to return **Recordset** objects.</span></span> <span data-ttu-id="ea6a3-121">Si une commande retournant des lignes s’exécute correctement mais ne retourne aucun enregistrement, l’objet **Recordset** retourné sera ouvert mais vide.</span><span class="sxs-lookup"><span data-stu-id="ea6a3-121">If a row-returning command executes successfully but returns no records, the returned **Recordset** object will be open but empty.</span></span> <span data-ttu-id="ea6a3-122">Dans ce cas de test en vérifiant que les propriétés [BOF](bof-eof-properties-ado.md) et [EOF](bof-eof-properties-ado.md) sont toutes deux **la valeur True**.</span><span class="sxs-lookup"><span data-stu-id="ea6a3-122">Test for this case by verifying that the [BOF](bof-eof-properties-ado.md) and [EOF](bof-eof-properties-ado.md) properties are both **True**.</span></span> <span data-ttu-id="ea6a3-123">Si une commande ne retournant pas ligne s’exécute correctement, l’objet **Recordset** retourné sera être fermé, ce que vous pouvez vérifier en testant la propriété [State](state-property-ado.md) sur le **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="ea6a3-123">If a non–row-returning command executes successfully, the returned **Recordset** object will be closed, which you can verify by testing the [State](state-property-ado.md) property on the **Recordset**.</span></span> <span data-ttu-id="ea6a3-124">Lorsqu’il n’y a aucune davantage de résultats, *jeu d’enregistrements* est définie sur *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="ea6a3-124">When there are no more results, *recordset* will be set to *Nothing*.</span></span>

<span data-ttu-id="ea6a3-125">La méthode **NextRecordset** n'est pas disponible sur un objet **Recordset** déconnecté, dont la propriété [ActiveConnection](activeconnection-property-ado.md) a la valeur **Nothing** (en Microsoft Visual Basic) ou NULL (dans les autres langages).</span><span class="sxs-lookup"><span data-stu-id="ea6a3-125">The **NextRecordset** method is not available on a disconnected **Recordset** object, where [ActiveConnection](activeconnection-property-ado.md) has been set to **Nothing** (in Microsoft Visual Basic) or NULL (in other languages).</span></span>

<span data-ttu-id="ea6a3-126">Si une modification est en cours en mode de mise à jour immédiate, l'appel de la méthode **NextRecordset** génère une erreur ; il faut d'abord appeler la méthode [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="ea6a3-126">If an edit is in progress while in immediate update mode, calling the **NextRecordset** method generates an error; call the [Update](update-method-ado.md) or [CancelUpdate](cancelupdate-method-ado.md) method first.</span></span>

<span data-ttu-id="ea6a3-p105">Pour passer des paramètres à plusieurs commandes dans l'instruction composée en complétant la collection [Parameters](parameters-collection-ado.md) ou en passant un tableau avec l'appel de **Open** ou **Execute** d'origine, les paramètres de la collection ou du tableau doivent respecter le même ordre que leurs commandes correspondantes dans la série de commandes. Vous devez terminer la lecture de tous les résultats avant de lire les valeurs des paramètres de sortie.</span><span class="sxs-lookup"><span data-stu-id="ea6a3-p105">To pass parameters for more than one command in the compound statement by filling the [Parameters](parameters-collection-ado.md) collection, or by passing an array with the original **Open** or **Execute** call, the parameters must be in the same order in the collection or array as their respective commands in the command series. You must finish reading all the results before reading output parameter values.</span></span>

<span data-ttu-id="ea6a3-p106">Votre fournisseur OLE DB détermine le moment où chaque commande d'une instruction composée est exécutée. Le [fournisseur Microsoft OLE DB pour SQL Server](microsoft-ole-db-provider-for-sql-server.md), par exemple, exécute toutes les commandes dans un lot lorsqu'il reçoit l'instruction composée. Les objets **Recordset** résultants sont simplement retournés lorsque vous appelez **NextRecordset**.</span><span class="sxs-lookup"><span data-stu-id="ea6a3-p106">Your OLE DB provider determines when each command command in a compound statement is executed. The [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), for example, executes all commands in a batch upon receiving the compound statement. The resulting **Recordsets** are simply returned when you call **NextRecordset**.</span></span>

<span data-ttu-id="ea6a3-p107">En revanche, il est possible que d'autres fournisseurs n'exécutent la commande suivante d'une instruction qu'après l'appel de NextRecordset. Pour ces fournisseurs, si vous fermez explicitement l'objet **Recordset** avant d'exécuter toute l'instruction, commande par commande, ADO n'exécute jamais les commandes restantes.</span><span class="sxs-lookup"><span data-stu-id="ea6a3-p107">However, other providers may execute the next command in a statement only after NextRecordset is called. For these providers, if you explicitly close the **Recordset** object before stepping through the entire command statement, ADO never executes the remaining commands.</span></span>

