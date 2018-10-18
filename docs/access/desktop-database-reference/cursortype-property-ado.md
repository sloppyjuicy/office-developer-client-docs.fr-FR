---
<<<<<<< Titre tête : propriété CursorType (ADO) TOCTitle : propriété CursorType (ADO) === titre : CursorType, propriété (ADO) TOCTitle : CursorType, propriété (ADO)
>>>>>>> Master ms:assetid : f42ded8f-9f92-ef03-a198-ffb892324611 ms:mtpsurl : https://msdn.microsoft.com/library/JJ250239(v=office.15) ms:contentKeyID : ms.date 48548682 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="cursortype-property-ado"></a>CursorType, propriété (ADO)
=======
# <a name="cursortype-property-ado"></a>CursorType, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le type de curseur utilisé dans un objet [Recordset](recordset-object-ado.md).

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou retourne une valeur de [CursorTypeEnum](cursortypeenum.md). La valeur par défaut est **adOpenForwardOnly**.

## <a name="remarks"></a>Notes

Utilisez la propriété **CursorType** pour spécifier le type de curseur à utiliser à l'ouverture de l'objet **Recordset**.

Seule la valeur **adOpenStatic** est prise en charge si la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**. Si une valeur non prise en charge est définie, aucune erreur n'est générée et le type de curseur ( **CursorType** ) le plus similaire pris en charge est utilisé à la place.

Si un fournisseur ne prend pas en charge le type de curseur demandé, il peut renvoyer un autre type de curseur. La propriété **CursorType** change pour s'adapter au type de curseur utilisé à l'ouverture de l'objet [Recordset](recordset-object-ado.md). Pour vérifier les fonctionnalités spécifiques du curseur retourné, utilisez la méthode [Supports](supports-method-ado.md). Une fois que vous fermez l'objet **Recordset**, la propriété **CursorType** reprend sa valeur initiale.

Le tableau ci-après indique les fonctionnalités des fournisseurs (identifiées par les constantes de la méthode **Supports** ) nécessaires à chaque type de curseur.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Pour un jeu d'enregistrements de ce type de curseur</p></th>
<th><p>La méthode Supports doit renvoyer la valeur True pour toutes ces constantes</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>aucune</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p><strong>adMovePrevious</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P>Même si la méthode <STRONG>Supports</STRONG>(<STRONG>adUpdateBatch</STRONG>) peut avoir la valeur True pour les curseurs dynamiques ou avant uniquement, vous devez, pour les mises à jour par lot, utiliser un curseur de jeu de clés ou statique. Affectez à la propriété <A href="locktype-property-ado.md">LockType</A> la valeur <STRONG>adLockBatchOptimistic</STRONG> et à la propriété <STRONG>CursorLocation</STRONG> la valeur <STRONG>adUseClient</STRONG> pour activer le service de curseur pour OLE DB, nécessaire aux mises à jour par lot.</P>



La propriété **CursorType** est en lecture/écriture lorsque l'objet **Recordset** est fermé et en lecture seule lorsqu'il est ouvert.

**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un objet Recordset de côté client, la propriété **CursorType** peut avoir uniquement aux **adOpenStatic**.

