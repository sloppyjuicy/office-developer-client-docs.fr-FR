---
<<<<<<< Titre tête : TOCTitle de la propriété LockType (ADO) : propriété LockType (ADO) === titre : LockType, propriété (ADO) TOCTitle : LockType, propriété (ADO)
>>>>>>> Master ms:assetid : 1d2622dc-6cab-1b7f-98a8-97a41d5c047f ms:mtpsurl : https://msdn.microsoft.com/library/JJ248965(v=office.15) ms:contentKeyID : ms.date 48543589 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="locktype-property-ado"></a>LockType, propriété (ADO)
=======
# <a name="locktype-property-ado"></a>LockType, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le type des verrous placés sur les enregistrements pendant leur modification.

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur [LockTypeEnum](locktypeenum.md). La valeur par défaut est **adLockReadOnly**.

## <a name="remarks"></a>Remarques

Définissez la propriété **LockType** avant d'ouvrir un [Recordset](recordset-object-ado.md) pour spécifier le type de verrouillage que le fournisseur doit utiliser pour l'ouvrir. Lisez la propriété pour connaître le type de verrouillage utilisé sur un objet **Recordset** ouvert.

Les fournisseurs peuvent ne pas prendre en charge tous types de verrouillage. Si un fournisseur ne reconnaît pas le paramètre **LockType** demandé, il le remplacera par un autre type de verrouillage. Pour déterminer la fonctionnalité réelle de verrouillage disponible pour un objet **Recordset**, utilisez la méthode [Supports](supports-method-ado.md) avec **adUpdate** et **adUpdateBatch**.

Le paramètre **adLockPessimistic** n'est pas pris en charge si la valeur de la propriété [CursorLocation](cursorlocation-property-ado.md) est **adUseClient**. Si la valeur spécifiée n'est pas prise en charge, aucune erreur n'est générée ; c'est le **LockType** pris en charge le plus proche qui est utilisé.

La propriété **LockType** est accessible en lecture et en écriture lorsque le **Recordset** est fermé et en lecture seule lorsqu' il est ouvert.

**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un objet Recordset de côté client, la propriété **LockType** peut uniquement être définie **: adLockBatchOptimistic**.

