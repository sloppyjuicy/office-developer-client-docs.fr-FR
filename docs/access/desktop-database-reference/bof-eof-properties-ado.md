---
<<<<<<< Titre tête : BOF, EOF propriétés (ADO) TOCTitle : BOF, EOF propriétés (ADO) === titre : BOF, propriétés EOF (ADO) TOCTitle : BOF, propriétés EOF (ADO)
>>>>>>> Master ms:assetid : f797e140-5572-1a4d-9afc-285f6a3868a8 ms:mtpsurl : https://msdn.microsoft.com/library/JJ250260(v=office.15) ms:contentKeyID : ms.date 48548768 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="bof-eof-properties-ado"></a>BOF, EOF, propriétés (ADO)
=======
# <a name="bof-eof-properties-ado"></a>BOF, propriétés EOF (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

  - **BOF**  Indique que la position d'enregistrement actuelle se trouve avant le premier enregistrement d'un objet [Recordset](recordset-object-ado.md).

  - **EOF**  Indique que la position d'enregistrement actuelle se trouve après le dernier enregistrement d'un objet **Recordset**.

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Les propriétés **BOF** et **EOF** retournent des valeurs de type **Boolean**.

## <a name="remarks"></a>Notes

Utilisez les propriétés **BOF** et **EOF** pour déterminer si un objet **Recordset** contient des enregistrements ou si vous avez dépassé les limites d'un objet **Recordset** lorsque vous vous déplacez d'un enregistrement à l'autre.

La propriété **BOF** retourne la valeur **True** (-1) si la position d'enregistrement actuelle se trouve avant le premier enregistrement et la valeur **False** (0) si la position d'enregistrement actuelle se trouve au niveau du premier enregistrement ou après celui-ci.

La propriété **EOF** renvoie la valeur **True** si la position d'enregistrement actuelle se trouve après le dernier enregistrement et la valeur **False** si la position d'enregistrement actuelle se trouve au niveau du dernier enregistrement ou avant celui-ci.

Si l'une des propriétés **BOF** ou **EOF** a la valeur **True**, il n'y a pas d'enregistrement actif.

Si vous ouvrez un objet **Recordset** qui ne contient pas d’enregistrement, les propriétés **BOF** et **EOF** ont la valeur **True** (reportez-vous à la propriété [RecordCount](recordcount-property-ado.md) pour plus d’informations sur cet état d’un objet **Recordset**). Lorsque vous ouvrez un objet **Recordset** qui contient au moins un enregistrement, le premier enregistrement correspond au dernier enregistrement et les propriétés **BOF** et **EOF** ont la valeur **False**.

Si vous supprimez le dernier enregistrement encore présent dans l'objet **Recordset**, les propriétés **BOF** et **EOF** peuvent conserver la valeur **False** jusqu'à ce que vous tentiez de repositionner l'enregistrement actif.

Ce tableau répertorie les méthodes **Move** autorisées avec les différentes combinaisons des propriétés **BOF** et **EOF**.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>MoveFirst,<br />
MoveLast</p></th>
<th><p>MovePrevious,<br />
Déplacer &lt; 0</p></th>
<th><p><br />
Move 0</p></th>
<th><p>MoveNext,<br />
Déplacer &gt; 0</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>BOF = True,</strong><br />
<strong>EOF = False</strong></p></td>
<td><p>Autorisé</p></td>
<td><p>Erreur</p></td>
<td><p>Erreur</p></td>
<td><p>Autorisé</p></td>
</tr>
<tr class="even">
<td><p><strong>BOF = False,</strong><br />
<strong>EOF = True</strong></p></td>
<td><p>Autorisé</p></td>
<td><p>Autorisé</p></td>
<td><p>Erreur</p></td>
<td><p>Erreur</p></td>
</tr>
<tr class="odd">
<td><p>Les deux propriétés ont la valeur <strong>True</strong></p></td>
<td><p>Erreur</p></td>
<td><p>Erreur</p></td>
<td><p>Erreur</p></td>
<td><p>Erreur</p></td>
</tr>
<tr class="even">
<td><p>Les deux propriétés ont la valeur <strong>False</strong></p></td>
<td><p>Autorisé</p></td>
<td><p>Autorisé</p></td>
<td><p>Autorisé</p></td>
<td><p>Autorisé</p></td>
</tr>
</tbody>
</table>


Même si une méthode **Move** est autorisée, rien ne garantit que la méthode parviendra à localiser un enregistrement. Cela signifie uniquement que l'appel de la méthode **Move** spécifiée ne génère pas d'erreur.

Le tableau ci-dessous répertorie les valeurs prises par les propriétés **BOF** et **EOF** lorsque vous appelez différentes méthodes **Move** et que vous ne parvenez pas à trouver un enregistrement.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p></p></th>
<th><p>BOF</p></th>
<th><p>EOF</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>MoveFirst</strong>, <strong>MoveLast</strong></p></td>
<td><p>La valeur <strong>True</strong></p></td>
<td><p>La valeur <strong>True</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Move</strong> 0</p></td>
<td><p>Aucune modification</p></td>
<td><p>Aucune modification</p></td>
</tr>
<tr class="odd">
<td><p><strong>MovePrevious</strong>, <strong>déplacer</strong> &lt; 0</p></td>
<td><p>Prend la valeur <strong>True</strong></p></td>
<td><p>Aucune modification</p></td>
</tr>
<tr class="even">
<td><p><strong>MoveNext</strong>, <strong>déplacer</strong> &gt; 0</p></td>
<td><p>Aucune modification</p></td>
<td><p>Prend la valeur <strong>True</strong></p></td>
</tr>
</tbody>
</table>

