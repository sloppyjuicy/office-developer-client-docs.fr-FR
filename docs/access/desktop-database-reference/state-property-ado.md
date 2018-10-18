---
<<<<<<< Titre tête : TOCTitle état propriété (ADO) : état de propriété (ADO) === titre : State, propriété (ADO) TOCTitle : State, propriété (ADO)
>>>>>>> Master ms:assetid : ade0a50c-e2d8-23ac-4ea9-b012fedcd5db ms:mtpsurl : https://msdn.microsoft.com/library/JJ249819(v=office.15) ms:contentKeyID : ms.date 48547053 : 18/09/2015 mtps_version : v=office.15 f1_keywords :
- Ado210.chm1231176 f1_categories :
- Office.Version=v15
---

<<<<<<< Tête
# <a name="state-property-ado"></a>State, propriété (ADO)
=======
# <a name="state-property-ado"></a>State, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique, pour tous les objets applicables, si l'état de l'objet est ouvert ou fermé.

Indique, pour tous les objets applicables exécutant une méthode asynchrone, si l'état actuel de l'objet est « en cours de connexion », « en cours d'exécution » ou « en cours d'extraction ».

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Renvoie une valeur de type **Long** pouvant être une valeur [ObjectStateEnum](objectstateenum.md). La valeur par défaut est **adStateClosed**.

## <a name="remarks"></a>Remarques

Vous pouvez utiliser à tout moment la propriété **State** pour déterminer l'état actuel d'un objet donné.

La propriété **State** de l'objet peut présenter plusieurs valeurs associées. Par exemple, si une instruction est en cours d'exécution, cette propriété aura la valeur **adStateOpen** associée à **adStateExecuting**.

La propriété **State** est en lecture seule.

