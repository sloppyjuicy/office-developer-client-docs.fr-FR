---
title: Recordset.AbsolutePosition Property (DAO)
TOCTitle: AbsolutePosition Property
ms:assetid: c35c0c07-f789-524b-0a3d-dfd18fa6eebc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823038(v=office.15)
ms:contentKeyID: 48547569
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c13dc234fc70d8cf5e9b14958b5336c39a6a4d7a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886507"
---
# <a name="recordsetabsoluteposition-property-dao"></a><span data-ttu-id="190eb-102">Recordset.AbsolutePosition Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="190eb-102">Recordset.AbsolutePosition Property (DAO)</span></span>

<span data-ttu-id="190eb-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="190eb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="190eb-104">Définit ou renvoie le numéro d’enregistrement relatif de l’enregistrement actif d’un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="190eb-104">Sets or returns the relative record number of a **Recordset** object's current record.</span></span>

## <a name="syntax"></a><span data-ttu-id="190eb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="190eb-105">Syntax</span></span>

<span data-ttu-id="190eb-106">*expression* . AbsolutePosition</span><span class="sxs-lookup"><span data-stu-id="190eb-106">*expression* .AbsolutePosition</span></span>

<span data-ttu-id="190eb-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="190eb-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="190eb-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="190eb-108">Remarks</span></span>

<span data-ttu-id="190eb-p101">Vous pouvez utiliser la propriété **AbsolutePosition** pour positionner le pointeur de l'enregistrement actif sur un enregistrement spécifique en fonction de sa position ordinale dans un objet **Recordset** de type feuille de réponse dynamique ou instantané. En outre, vous pouvez déterminer le numéro de l'enregistrement actif en consultant le paramétrage de la propriété **AbsolutePosition**.</span><span class="sxs-lookup"><span data-stu-id="190eb-p101">You can use the **AbsolutePosition** property to position the current record pointer to a specific record based on its ordinal position in a dynaset- or snapshot-type **Recordset** object. You can also determine the current record number by checking the **AbsolutePosition** property setting.</span></span>

<span data-ttu-id="190eb-p102">La valeur de la propriété **AbsolutePosition** est basée sur zéro, c'est-à-dire que la valeur 0 fait référence au premier enregistrement de l'objet **Recordset**. Par conséquent, il est impossible de la définir sur une valeur supérieure ou égale au nombre d'enregistrements renseignés, sinon vous obtenez une erreur interceptable. Pour connaître le nombre d'enregistrements renseignés dans l'objet **Recordset**, consultez le paramétrage de la propriété **RecordCount**. La valeur maximale autorisée de la propriété **AbsolutePosition** correspond à la valeur de la propriété **RecordCount** moins 1.</span><span class="sxs-lookup"><span data-stu-id="190eb-p102">Because the **AbsolutePosition** property value is zero-based (that is, a setting of 0 refers to the first record in the **Recordset** object), you cannot set it to a value greater than or equal to the number of populated records; doing so causes a trappable error. You can determine the number of populated records in the **Recordset** object by checking the **RecordCount** property setting. The maximum allowable setting for the **AbsolutePosition** property is the value of the **RecordCount** property minus 1.</span></span>

<span data-ttu-id="190eb-114">Si aucun enregistrement actif, en tant que lorsqu’il n’y a aucun enregistrement dans l’objet **Recordset** , **la propriété AbsolutePosition** renvoie -1.</span><span class="sxs-lookup"><span data-stu-id="190eb-114">If there is no current record, as when there are no records in the **Recordset** object, **AbsolutePosition** returns –1.</span></span> <span data-ttu-id="190eb-115">Si l'enregistrement actif est supprimé, la valeur de la propriété **AbsolutePosition** n'est pas définie et une erreur interceptable se produit s'il est référencé.</span><span class="sxs-lookup"><span data-stu-id="190eb-115">If the current record is deleted, the **AbsolutePosition** property value isn't defined, and a trappable error occurs if it's referenced.</span></span> <span data-ttu-id="190eb-116">Les nouveaux enregistrements sont ajoutés à la fin de la séquence.</span><span class="sxs-lookup"><span data-stu-id="190eb-116">New records are added to the end of the sequence.</span></span>

<span data-ttu-id="190eb-p104">N'utilisez pas cette propriété en tant que numéro d'enregistrement de substitution. Pour conserver une position donnée et y revenir, il est toujours recommandé d'utiliser des signets. En outre, il s'agit de la seule manière de positionner l'enregistrement actif sur tous les types d'objets **Recordset**. Plus particulièrement, la position d'un enregistrement change lors de la suppression d'un ou plusieurs enregistrements qui le précèdent. En outre, il n'est pas certain qu'un enregistrement aura la même position absolue si l'objet **Recordset** est recréé, car l'ordre des enregistrements d'un objet **Recordset** n'est garanti que s'il est créé avec une instruction SQL à l'aide d'une clause ORDER BY.</span><span class="sxs-lookup"><span data-stu-id="190eb-p104">You shouldn't use this property as a surrogate record number. Bookmarks are still the recommended way of retaining and returning to a given position and are the only way to position the current record across all types of **Recordset** objects. In particular, the position of a record changes when one or more records preceding it are deleted. There is also no assurance that a record will have the same absolute position if the **Recordset** object is re-created again because the order of individual records within a **Recordset** object isn't guaranteed unless it's created with an SQL statement by using an ORDER BY clause.</span></span>

> [!NOTE]
> - <span data-ttu-id="190eb-p105">Si vous définissez la propriété **AbsolutePosition** sur une valeur supérieure à zéro pour un nouvel objet **Recordset** ouvert mais non renseigné, vous obtenez une erreur interceptable. Renseignez d'abord l'objet **Recordset** à l'aide de la méthode **MoveLast**.</span><span class="sxs-lookup"><span data-stu-id="190eb-p105">Setting the **AbsolutePosition** property to a value greater than zero on a newly opened but unpopulated **Recordset** object causes a trappable error. Populate the **Recordset** object first with the **MoveLast** method.</span></span>
> - <span data-ttu-id="190eb-123">La propriété **AbsolutePosition** n’est pas disponible pour les objets **Recordset** de type avant uniquement ou les objets **Recordset** ouverts à partir de requêtes directes sur des bases de données ODBC connectées au moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="190eb-123">The **AbsolutePosition** property isn't available on forward–only–type **Recordset** objects, or on **Recordset** objects opened from pass-through queries against Microsoft Access database engine-connected ODBC databases.</span></span>

## <a name="example"></a><span data-ttu-id="190eb-124">Exemple</span><span class="sxs-lookup"><span data-stu-id="190eb-124">Example</span></span>

<span data-ttu-id="190eb-125">L'exemple ci-dessous utilise la propriété **AbsolutePosition** pour effectuer le suivi de la progression d'une boucle qui énumère tous les enregistrements d'un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="190eb-125">This example uses the **AbsolutePosition** property to track the progress of a loop that enumerates all the records of a **Recordset**.</span></span>

```vb
    Sub AbsolutePositionX() 
     
       Dim dbsNorthwind As Database 
       Dim rstEmployees As Recordset 
       Dim strMessage As String 
     
       Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
       ' AbsolutePosition only works with dynasets or snapshots. 
       Set rstEmployees = _ 
          dbsNorthwind.OpenRecordset("Employees", _ 
          dbOpenSnapshot) 
     
       With rstEmployees 
          ' Populate Recordset. 
          .MoveLast 
          .MoveFirst 
     
          ' Enumerate Recordset. 
          Do While Not .EOF 
             ' Display current record information. Add 1 to  
             ' AbsolutePosition value because it is zero-based. 
             strMessage = "Employee: " & !LastName & vbCr & _ 
                "(record " & (.AbsolutePosition + 1) & _ 
                " of " & .RecordCount & ")" 
             If MsgBox(strMessage, vbOKCancel) = vbCancel _ 
                Then Exit Do 
             .MoveNext 
          Loop 
     
          .Close 
       End With 
     
       dbsNorthwind.Close 
     
    End Sub
```
