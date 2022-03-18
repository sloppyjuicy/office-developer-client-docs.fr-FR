---
title: Interface ADORecordsetConstruction (ADO)
TOCTitle: ADORecordsetConstruction interface (ADO)
ms:assetid: 2b53aa6e-3b6f-a996-3967-534215fd586c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249060(v=office.15)
ms:contentKeyID: 48543926
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a0d18c4fab3a3103315be739a5c8dd3ea90f987a
ms.sourcegitcommit: 2d91bac3a93af3f1f73098f484000ba2a6377cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/17/2022
ms.locfileid: "63558347"
---
# <a name="adorecordsetconstruction-interface-ado"></a>Interface ADORecordsetConstruction (ADO)


**S’applique à** : Access 2013, Office 2013

L'interface **ADORecordsetConstruction** permet de créer un objet **Recordset** ADO à partir d'un objet **Rowset** OLE DB dans une application C/C++.

Cette interface prend en charge les propriétés ci-après :

## <a name="properties"></a>Propriétés

<table>
<colgroup>
<col />
<col />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="chapter-property-ado.md">Chapitre</a></p></td>
<td><p>Lecture/écriture.<br />
 Extrait/définit un objet <strong>Chapter</strong> OLE DB de/sur cet objet <strong>Recordset</strong> ADO.</p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>Lecture/écriture.<br />
 Extrait/définit un objet <strong>RowPosition</strong> OLE DB de/sur cet objet <strong>Recordset</strong> ADO.</p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">Rowset</a></p></td>
<td><p>Lecture/écriture.<br />
 Extrait/définit un objet <strong>Rowset</strong> OLE DB de/sur cet objet <strong>Recordset</strong> ADO.</p></td>
</tr>
</tbody>
</table>


## <a name="methods"></a>Méthodes

Aucun.

## <a name="events"></a>Événements

Aucun.

## <a name="remarks"></a>Remarques

Étant donné un objet **Rowset** OLE DB (pRowset ), la construction d’un objet **Recordset** ADO (), la construction d’un objet **Recordset** ADO (adoRs) revient aux trois opérations de base suivantes :

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

3. Appelez la méthode de propriété IADORecordsetConstruction::p utRowset\_ pour définir l’objet Rowset OLE DB sur l’objet Recordset ADO :

   ```vb     
    IUnknown *pUnk=NULL;
    pRowset->QueryInterface(IID_IUnknown, (void**)&pUnk);
    adoRsConstruct->put_Rowset(pUnk);
   ```
L’objet résultant représente désormais l’objet **Recordset** ADO construit à partir de l’objet **Rowset** OLE DB.

Vous pouvez également créer un objet **Recordset** ADO à partir d'un objet **Chapter** ou **RowPosition** OLE DB.

## <a name="requirements"></a>Conditions requises

- **Version :** ADO 2.0 et supérieure

- **Bibliothèque :** msado15.dll

- **UUID :** 00000283-0000-0010-8000-00AA006D2EA4

