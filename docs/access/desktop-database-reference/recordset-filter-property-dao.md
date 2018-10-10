---
title: Propriété Recordset.Filter (DAO)
TOCTitle: Filter Property
ms:assetid: feffa23b-c348-9718-ba4b-65db0f739789
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837300(v=office.15)
ms:contentKeyID: 48548953
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 906c3bd9e437ca5fc64067530ecbcaa033ea52d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470481"
---
# <a name="recordsetfilter-property-dao"></a><span data-ttu-id="0e0de-102">Propriété Recordset.Filter (DAO)</span><span class="sxs-lookup"><span data-stu-id="0e0de-102">Recordset.Filter Property (DAO)</span></span>

<span data-ttu-id="0e0de-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e0de-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0e0de-p101">Définit ou renvoie une valeur qui détermine les enregistrements inclus dans un objet **Recordset** ouvert par la suite (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="0e0de-p101">Sets or returns a value that determines the records included in a subsequently opened **Recordset** object (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e0de-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e0de-106">Syntax</span></span>

<span data-ttu-id="0e0de-107">*expression* . Filtre</span><span class="sxs-lookup"><span data-stu-id="0e0de-107">*expression* .Filter</span></span>

<span data-ttu-id="0e0de-108">*expression* Expression qui renvoie un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="0e0de-108">*expression* An expression that returns a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e0de-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="0e0de-109">Remarks</span></span>

<span data-ttu-id="0e0de-110">Le paramètre ou la valeur de retour est un type de données String qui contient une clause WHERE d'une instruction SQL sans le mot réservé WHERE.</span><span class="sxs-lookup"><span data-stu-id="0e0de-110">The setting or return value is a String data type that contains the WHERE clause of an SQL statement without the reserved word WHERE.</span></span>

<span data-ttu-id="0e0de-111">Utilisez la propriété **Filter** pour appliquer un filtre à un objet **Recordset** de type avant uniquement, instantané ou feuille de réponse dynamique.</span><span class="sxs-lookup"><span data-stu-id="0e0de-111">Use the **Filter** property to apply a filter to a dynaset–, snapshot–, or forward–only–type **Recordset** object.</span></span>

<span data-ttu-id="0e0de-112">La propriété **Filter** permet de limiter le nombre d'enregistrements renvoyés à partir d'un objet existant lorsqu'un nouvel objet **Recordset** est ouvert sur la base d'un objet **Recordset** existant.</span><span class="sxs-lookup"><span data-stu-id="0e0de-112">You can use the **Filter** property to restrict the records returned from an existing object when a new **Recordset** object is opened based on an existing **Recordset** object.</span></span>

<span data-ttu-id="0e0de-113">Utilisez le format de date américain (mois-jour-année) lorsque vous filtrez des champs contenant des dates, même si vous n’utilisez pas la version de moteur de base de données Microsoft Access (dans ce cas, vous devez assembler les dates en concaténant des chaînes, par exemple strMonth & «- » & strDay & «- » & strYear).</span><span class="sxs-lookup"><span data-stu-id="0e0de-113">Use the U.S. date format (month-day-year) when you filter fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine (in which case you must assemble any dates by concatenating strings, for example, strMonth & "-" & strDay & "-" & strYear).</span></span> <span data-ttu-id="0e0de-114">Sinon, il est possible que le filtrage des données ne donne pas les résultats escomptés.</span><span class="sxs-lookup"><span data-stu-id="0e0de-114">Otherwise, the data may not be filtered as you expect.</span></span>

<span data-ttu-id="0e0de-115">Dans la plupart des cas, il est plus rapide d'ouvrir un nouvel objet **Recordset** à l'aide d'une instruction SQL qui inclut une clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="0e0de-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes a WHERE clause.</span></span>

<span data-ttu-id="0e0de-116">Si vous définissez la propriété une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strFilter = « prix \> » & lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez de Ouvrez le prochain **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="0e0de-116">If you set the property to a string concatenated with a non–integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strFilter = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the next **Recordset**.</span></span> <span data-ttu-id="0e0de-117">En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.</span><span class="sxs-lookup"><span data-stu-id="0e0de-117">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

## <a name="example"></a><span data-ttu-id="0e0de-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="0e0de-118">Example</span></span>

<span data-ttu-id="0e0de-119">L'exemple suivant montre comment utiliser la propriété Filter pour déterminer les enregistrements à inclure dans un Recordset ouvert par la suite.</span><span class="sxs-lookup"><span data-stu-id="0e0de-119">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

<span data-ttu-id="0e0de-120">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="0e0de-120">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```
