---
<<<<<<< Titre tête : Index propriété (ADO) TOCTitle : Index de propriété (ADO) === titre : Index, propriété (ADO) TOCTitle : Index, propriété (ADO)
>>>>>>> Master ms:assetid : 4cc00521-dcb4-19b2-2174-6e0e9bd42e62 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249241(v=office.15) ms:contentKeyID : ms.date 48544715 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="index-property-ado"></a>Index, propriété (ADO)
=======
# <a name="index-property-ado"></a>Index, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le nom de l'index utilisé pour un objet [Recordset](recordset-object-ado.md).

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur **String** indiquant le nom de l'index.

## <a name="remarks"></a>Remarques

L'index nommé par la propriété **Index** doit avoir été préalablement déclaré sur la table de base sous-jacente de l'objet **Recordset**. C'est-à-dire que l'index doit avoir été déclaré par programmation soit sous forme d'objet [Index](index-object-adox.md) ADOX, soit au moment de la création de la table de base.

Une erreur d'exécution est générée si l'index ne peut pas être défini. La propriété **Index** ne peut pas être définie :

  - Dans un gestionnaire d'événements [WillChangeRecordset](willchangerecordset-and-recordsetchangecomplete-events-ado.md) ou **RecordsetChangeComplete**.

  - Si le **Recordset** exécute encore une opération (ce qui peut être déterminé par la propriété [State](state-property-ado.md)).

  - Si un filtre a été défini sur le **Recordset** par la propriété [Filter](filter-property-ado.md).

La propriété **Index** peut toujours être définie avec succès si le **Recordset** est fermé, mais le **Recordset** ne s'ouvre pas correctement (ou l'index n'est pas utilisable) si le fournisseur sous-jacent ne prend pas en charge les index.

Si l'index peut être défini, il se peut que la position de la ligne active soit modifiée. Cela provoque la mise à jour de la propriété [AbsolutePosition](absoluteposition-property-ado.md) et la génération des événements **WillChangeRecordset**, **RecordsetChangeComplete**, [WillMove](willmove-and-movecomplete-events-ado.md) et [MoveComplete](willmove-and-movecomplete-events-ado.md).

Si l'index peut être défini et que la valeur de la propriété [LockType](locktype-property-ado.md) est **adLockPessimistic** ou **adLockOptimistic**, une opération [UpdateBatch](updatebatch-method-ado.md) implicite est réalisée. Cela libère le groupe actuel et le groupe attribué. S'il existe un filtre, il est libéré, et la ligne active devient la première ligne du **Recordset** réorganisé.

La propriété **Index** est utilisée en association avec la méthode [Seek](seek-method-ado.md). Si le fournisseur sous-jacent ne prend pas en charge la propriété **Index** (et donc la méthode **Seek** ), pensez à utiliser plutôt la méthode [Find](find-method-ado.md). Déterminer si l’objet **Recordset** prend en charge les index avec la méthode **(adIndex)** [prend en charge](supports-method-ado.md).

La propriété **Index** intégrée n'a aucun rapport avec la propriété [Optimize](optimize-property-dynamic-ado.md) dynamique, même si toutes deux portent sur les index.

