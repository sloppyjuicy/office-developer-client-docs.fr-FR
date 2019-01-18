---
title: ADORecordsetConstruction, interface (ADO)
TOCTitle: ADORecordsetConstruction interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 98342d5456c545e6da8539c11f616c08fd52a932
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701277"
---
# <a name="adorecordsetconstruction-interface-ado"></a>ADORecordsetConstruction, interface (ADO)


**S’applique à**: Access 2013, Office 2013

L'interface **ADORecordsetConstruction** permet de créer un objet **Recordset** ADO à partir d'un objet **Rowset** OLE DB dans une application C/C++.

Cette interface prend en charge les propriétés ci-après :

## <a name="properties"></a>Propriétés

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="chapter-property-ado.md">Chapitre</a></p></td>
<td><p>Lecture/écriture.<br />
Obtient ou définit un objet OLE DB <strong>chapitre</strong> à partir de/sur cet objet ADO <strong>Recordset</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>Lecture/écriture.<br />
Obtient ou définit un objet OLE DB <strong>RowPosition</strong> à partir de/sur cet objet ADO <strong>Recordset</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">Ensemble de lignes</a></p></td>
<td><p>Lecture/écriture.<br />
Obtient ou définit un objet OLE DB <strong>Rowset</strong> à partir de/sur cet objet ADO <strong>Recordset</strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Méthodes

Aucune.

## <a name="events"></a>Événements

Aucun.

## <a name="remarks"></a>Remarques

Étant donné un objet OLE DB **Rowset** (pRowset), la construction d’un objet de ADO **Recordset** (), la construction d’un objet **Recordset** ADO les chiffres d’objet (adoRs) pour les trois opérations ci-après :

1. Créez un objet **Recordset** ADO :
    
   ```vb
    Recordset20Ptr adoRs;
    adoRs.CreateInstance(__uuidof(Recordset));
   ```
2. Interrogez l'interface **IADORecordsetConstruction** sur l'objet **Recordset**:

   ```vb    
    adoRecordsetConstructionPtr adoRsConstruct=NULL;
    adoRs->QueryInterface(__uuidof(ADORecordsetConstruction),
         (void**)&adoRsConstruct);
   ```

3. Appelez le IADORecordsetConstruction::put\_méthode de la propriété Rowset pour définir l’objet Rowset OLE DB sur l’objet Recordset ADO :

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
L’objet qui en résulte représente maintenant l’objet de l’objet **Recordset** ADO construit à partir de l’objet OLE DB **Rowset** .

Vous pouvez également créer un objet **Recordset** ADO à partir d'un objet **Chapter** ou **RowPosition** OLE DB.

## <a name="requirements"></a>Configuration requise

- **Version :** ADO 2.0 et supérieure

- **Bibliothèque :** msado15.dll

- **UUID :** 00000283-0000-0010-8000-00AA006D2EA4

