---
title: ADORecordConstruction, interface (ADO)
TOCTitle: ADORecordConstruction Interface (ADO)
ms:assetid: 3f0afbdb-f1c4-e44e-7c0f-a0c4cee554a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249175(v=office.15)
ms:contentKeyID: 48544387
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 44272067d8018836fd7eb3d6cfaa762780f69868
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470799"
---
# <a name="adorecordconstruction-interface-ado"></a><span data-ttu-id="dbc92-102">ADORecordConstruction, interface (ADO)</span><span class="sxs-lookup"><span data-stu-id="dbc92-102">ADORecordConstruction Interface (ADO)</span></span>


<span data-ttu-id="dbc92-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="dbc92-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dbc92-104">L'interface **ADORecordConstruction** permet de créer un objet **Record** ADO à partir d'un objet **Row** OLE DB dans une application C/C++.</span><span class="sxs-lookup"><span data-stu-id="dbc92-104">The **ADORecordConstruction** interface is used to construct an ADO **Record** object from an OLE DB **Row** object in a C/C++ application.</span></span>

<span data-ttu-id="dbc92-105">Cette interface prend en charge les propriétés ci-après :</span><span class="sxs-lookup"><span data-stu-id="dbc92-105">This interface supports the following properties:</span></span>

## <a name="properties"></a><span data-ttu-id="dbc92-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="dbc92-106">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dbc92-107"><a href="parentrow-property-ado.md">Ligne parente</a></span><span class="sxs-lookup"><span data-stu-id="dbc92-107"><a href="parentrow-property-ado.md">ParentRow</a></span></span></p></td>
<td><p><span data-ttu-id="dbc92-108">En écriture seule.</span><span class="sxs-lookup"><span data-stu-id="dbc92-108">Write-only.</span></span><br />
<span data-ttu-id="dbc92-109">Définit le conteneur d’un objet OLE DB <strong>Row</strong> sur cet objet ADO <strong>Record</strong> .</span><span class="sxs-lookup"><span data-stu-id="dbc92-109">Sets the container of an OLE DB <strong>Row</strong> object on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dbc92-110"><a href="row-property-ado.md">Row</a></span><span class="sxs-lookup"><span data-stu-id="dbc92-110"><a href="row-property-ado.md">Row</a></span></span></p></td>
<td><p><span data-ttu-id="dbc92-111">En lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="dbc92-111">Read/Write.</span></span><br />
<span data-ttu-id="dbc92-112">Obtient ou définit un objet OLE DB <strong>Row</strong> à partir de/sur cet objet ADO <strong>Record</strong> .</span><span class="sxs-lookup"><span data-stu-id="dbc92-112">Gets/sets an OLE DB <strong>Row</strong> object from/on this ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a><span data-ttu-id="dbc92-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="dbc92-113">Methods</span></span>

<span data-ttu-id="dbc92-114">Aucune.</span><span class="sxs-lookup"><span data-stu-id="dbc92-114">None.</span></span>

## <a name="events"></a><span data-ttu-id="dbc92-115">Événements</span><span class="sxs-lookup"><span data-stu-id="dbc92-115">Events</span></span>

<span data-ttu-id="dbc92-116">Aucune.</span><span class="sxs-lookup"><span data-stu-id="dbc92-116">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbc92-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="dbc92-117">Remarks</span></span>

<span data-ttu-id="dbc92-118">Étant donné un objet OLE DB **Row** (pRow), la construction d’un objet de ADO **Record** (), la construction d’un objet ADO **Record** (adoR), les chiffres à trois opérations ci-après :</span><span class="sxs-lookup"><span data-stu-id="dbc92-118">Given an OLE DB **Row** object (pRow), the construction of an ADO **Record** object (), the construction of an ADO **Record** object (adoR), amounts to the following three basic operations:</span></span>

1.  <span data-ttu-id="dbc92-119">Créez un objet ADO **Record**:</span><span class="sxs-lookup"><span data-stu-id="dbc92-119">Create an ADO **Record** object:</span></span>
    
    ```vb
        _RecordPtr adoR;
        adoRs.CreateInstance(__uuidof(_Record));
    ```

2.  <span data-ttu-id="dbc92-120">Interrogez l'interface **IADORecordConstruction** sur l'objet **Record**:</span><span class="sxs-lookup"><span data-stu-id="dbc92-120">Query the **IADORecordConstruction** interface on the **Record** object:</span></span>
    
    ```vb
        adoRecordConstructionPtr adoRConstruct=NULL;
        adoR->QueryInterface(__uuidof(ADORecordConstruction),
                            (void**)&adoRConstruct);
    ```

3.  <span data-ttu-id="dbc92-121">Appelez le **IADORecordConstruction::put\_ligne** méthode de la propriété pour définir l’objet OLE DB **Row** dans l’objet ADO **Record** :</span><span class="sxs-lookup"><span data-stu-id="dbc92-121">Call the **IADORecordConstruction::put\_Row** property method to set the OLE DB **Row** object on the ADO **Record** object:</span></span>
    
    ```vb
        IUnknown *pUnk=NULL;
        pRow->QueryInterface(IID_IUnknown, (void**)&pUnk);
        adoRConstruct->put_Row(pUnk);
    ```
    
<span data-ttu-id="dbc92-122">L'objet **adoR** qui en résulte représente maintenant l'objet **Record** ADO créé à partir de l'objet **Row** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="dbc92-122">The resultant **adoR** object now represents the ADO **Record** object constructed from the OLE DB **Row** object.</span></span>

<span data-ttu-id="dbc92-123">Un objet **Record** ADO peut également être créé à partir du conteneur d'un objet **Row** OLE DB.</span><span class="sxs-lookup"><span data-stu-id="dbc92-123">An ADO **Record** object can also be constructed from the container of an OLE DB **Row** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="dbc92-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dbc92-124">Requirements</span></span>

<span data-ttu-id="dbc92-125">**Version :** ADO 2.0 et supérieure</span><span class="sxs-lookup"><span data-stu-id="dbc92-125">**Version:** ADO 2.0 and later</span></span>

<span data-ttu-id="dbc92-126">**Bibliothèque :** msado15.dll</span><span class="sxs-lookup"><span data-stu-id="dbc92-126">**Library:** msado15.dll</span></span>

<span data-ttu-id="dbc92-127">**UUID :** 00000567-0000-0010-8000-00AA006D2EA4</span><span class="sxs-lookup"><span data-stu-id="dbc92-127">**UUID:** 00000567-0000-0010-8000-00AA006D2EA4</span></span>

