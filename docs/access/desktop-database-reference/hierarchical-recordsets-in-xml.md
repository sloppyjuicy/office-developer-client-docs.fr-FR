---
title: Jeux d'enregistrements hiérarchiques dans XML
TOCTitle: Hierarchical Recordsets in XML
ms:assetid: 606dee87-8762-6cc2-a151-94d34031b35f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249351(v=office.15)
ms:contentKeyID: 48545181
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f608cd8ed36b621847c58dd523cfa052c5f501a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471473"
---
# <a name="hierarchical-recordsets-in-xml"></a><span data-ttu-id="de12f-102">Jeux d'enregistrements hiérarchiques dans XML</span><span class="sxs-lookup"><span data-stu-id="de12f-102">Hierarchical Recordsets in XML</span></span>


<span data-ttu-id="de12f-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="de12f-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="hierarchical-recordsets-in-xml"></a><span data-ttu-id="de12f-104">Jeux d'enregistrements hiérarchiques dans XML</span><span class="sxs-lookup"><span data-stu-id="de12f-104">Hierarchical Recordsets in XML</span></span>

<span data-ttu-id="de12f-105">ADO autorise la persistance des objets **Recordset** hiérarchiques au format XML.</span><span class="sxs-lookup"><span data-stu-id="de12f-105">ADO allows persistence of hierarchical **Recordset** objects into XML.</span></span> <span data-ttu-id="de12f-106">Avec les objets **Recordset** hiérarchiques, la valeur d’un champ dans **l’objet Recordset** parent est un autre **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="de12f-106">With hierarchical **Recordset** objects, the value of a field in the parent **Recordset** is another **Recordset**.</span></span> <span data-ttu-id="de12f-107">Ces champs sont représentées comme éléments enfants dans le flux XML plutôt qu’un attribut.</span><span class="sxs-lookup"><span data-stu-id="de12f-107">Such fields are represented as child elements in the XML stream rather than an attribute.</span></span> <span data-ttu-id="de12f-108">L’exemple suivant illustre ce cas :</span><span class="sxs-lookup"><span data-stu-id="de12f-108">The following example demonstrates this case:</span></span>

```vb 
 
Rs.Open "SHAPE {select stor_id, stor_name, state from stores} APPEND ({select stor_id, ord_num, ord_date, qty from sales} AS rsSales RELATE stor_id TO stor_id)", "Provider=MSDataShape;DSN=pubs;UID=MyUserId;PWD=MyPassword;" 
```

<span data-ttu-id="de12f-109">L'exemple suivant représente le format XML du **jeu d'enregistrements** persistant :</span><span class="sxs-lookup"><span data-stu-id="de12f-109">The following is the XML format of the persisted **Recordset**:</span></span>

```xml 
 
<xml xmlns:s="uuid:BDC6E3F0-6DA3-11d1-A2A3-00AA00C14882"     xmlns:dt="uuid:C2F41010-65B3-11d1-A29F-00AA00C14882"     xmlns:rs="urn:schemas-microsoft-com:rowset"  
    xmlns:z="#RowsetSchema">  
  <s:Schema id="RowsetSchema">  
    <s:ElementType name="row" content="eltOnly" rs:updatable="true">  
      <s:AttributeType name="stor_id" rs:number="1"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="4"  
          rs:fixedlength="true" rs:maybenull="false"/>  
      </s:AttributeType>  
      <s:AttributeType name="stor_name" rs:number="2" rs:nullable="true"  
        rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="40"/>  
      </s:AttributeType>  
      <s:AttributeType name="state" rs:number="3" rs:nullable="true"  
        rs:writeunknown="true">  
        <s:datatype dt:type="string" dt:maxLength="2"  
          rs:fixedlength="true"/>  
      </s:AttributeType>  
      <s:ElementType name="rsSales" content="eltOnly"  
        rs:updatable="true" rs:relation="010000000100000000000000">  
        <s:AttributeType name="stor_id" rs:number="1"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="4"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_num" rs:number="2"  
          rs:writeunknown="true">  
          <s:datatype dt:type="string" dt:maxLength="20"  
            rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="ord_date" rs:number="3"  
          rs:writeunknown="true">  
            <s:datatype dt:type="dateTime" dt:maxLength="16"  
              rs:scale="3" rs:precision="23" rs:fixedlength="true"  
              rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:AttributeType name="qty" rs:number="4" rs:writeunknown="true">  
          <s:datatype dt:type="i2" dt:maxLength="2" rs:precision="5"  
            rs:fixedlength="true" rs:maybenull="false"/>  
        </s:AttributeType>  
        <s:extends type="rs:rowbase"/>  
      </s:ElementType>  
      <s:extends type="rs:rowbase"/>  
    </s:ElementType>  
  </s:Schema>  
  <rs:data>  
    <z:row stor_id="6380" stor_name="Eric the Read Books" state="WA">  
      <rsSales stor_id="6380" ord_num="6871"  
        ord_date="1994-09-14T00:00:00" qty="5"/>  
      <rsSales stor_id="6380" ord_num="722a"  
        ord_date="1994-09-13T00:00:00" qty="3"/>  
    </z:row>  
    <z:row stor_id="7066" stor_name="Barnum's" state="CA">  
      <rsSales stor_id="7066" ord_num="A2976"  
        ord_date="1993-05-24T00:00:00" qty="50"/>  
      <rsSales stor_id="7066" ord_num="QA7442.3"  
        ord_date="1994-09-13T00:00:00" qty="75"/>  
    </z:row>  
    <z:row stor_id="7067" stor_name="News & Brews" state="CA">  
      <rsSales stor_id="7067" ord_num="D4482"  
        ord_date="1994-09-14T00:00:00" qty="10"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="40"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
      <rsSales stor_id="7067" ord_num="P2121"  
        ord_date="1992-06-15T00:00:00" qty="20"/>  
    </z:row>  
... 
  </rs:data>  
</xml>  
```

<span data-ttu-id="de12f-p102">L'ordre exact des colonnes du **jeu d'enregistrements** parent n'est pas évident lorsqu'il est conservé de cette manière. Tout champ du parent peut contenir un **jeu d'enregistrements** enfant. Le fournisseur de persistance conserve d'abord toutes les colonnes scalaires en tant qu'attributs, puis toutes les « colonnes » du **jeu d'enregistrements** enfant comme des éléments enfants de la ligne parent. Vous pouvez obtenir la position ordinale du champ du **jeu d'enregistrements** en consultant la définition schématique du **jeu d'enregistrements**. Chaque champ comprend une propriété OLE DB, **rs:number**, définie dans l'espace de noms du schéma **Recordset** qui contient le nombre ordinal de ce champ.</span><span class="sxs-lookup"><span data-stu-id="de12f-p102">The exact order of the columns in the parent **Recordset** is not obvious when it is persisted in this manner. Any field in the parent may contain a child **Recordset**. The Persistence Provider persists out all scalar columns first as attributes and then persists out all child **Recordset** "columns" as child elements of the parent row. The ordinal position of the field in the parent **Recordset** can be obtained by looking at the schema definition of the **Recordset**. Every field has an OLE DB property, **rs:number**, defined in the **Recordset** schema namespace that contains the ordinal number for that field.</span></span>

<span data-ttu-id="de12f-p103">Les noms de tous les champs du **jeu d'enregistrements** enfant sont concaténés avec le nom du champ du **jeu d'enregistrements** parent dont il dépend. Ceci permet d'éviter les conflits de noms dans les cas où les **jeux d'enregistrements** enfant et parent contiennent tous les deux un champ obtenu à partir de deux tables différentes mais portant le même nom.</span><span class="sxs-lookup"><span data-stu-id="de12f-p103">The names of all fields in the child **Recordset** are concatenated with the name of the field in the parent **Recordset** that contains this child. This is to ensure that there are no name collisions in cases where parent and child **Recordsets** both contain a field that is obtained from two different tables but is named singularly.</span></span>

<span data-ttu-id="de12f-117">Lorsque vous enregistrez des **jeux d'enregistrements** hiérarchiques au format XML, gardez à l'esprit les restrictions suivantes dans ADO :</span><span class="sxs-lookup"><span data-stu-id="de12f-117">When saving hierarchical **Recordsets** into XML, you should be aware of the following restrictions in ADO:</span></span>

  - <span data-ttu-id="de12f-118">Un **jeu d'enregistrements** hiérarchique avec des mises à jour en suspens ne peut pas être conservé au format XML.</span><span class="sxs-lookup"><span data-stu-id="de12f-118">A hierarchical **Recordset** with pending updates cannot be persisted into XML.</span></span>

  - <span data-ttu-id="de12f-119">Un **jeu d'enregistrements** hiérarchique créé avec une commande de mise en forme paramétrée ne peut pas être conservé (que ce soit au format XML ou ADTG).</span><span class="sxs-lookup"><span data-stu-id="de12f-119">A hierarchical **Recordset** created with a parameterized shape command cannot be persisted (in either XML or ADTG format).</span></span>

  - <span data-ttu-id="de12f-p104">ADO enregistre actuellement la relation entre les **jeux d'enregistrements** enfant et parent en tant que BLOB. Les balises XML décrivant cette relation ne sont pas encore définies dans l'espace de noms du schéma du jeu de lignes.</span><span class="sxs-lookup"><span data-stu-id="de12f-p104">ADO currently saves the relationship between the parent and the child **Recordsets** as a binary large object (BLOB). XML tags to describe this relationship have not yet been defined in the rowset schema namespace.</span></span>

  - <span data-ttu-id="de12f-p105">Lorsque vous sauvegardez un **jeu d'enregistrements** hiérarchique, tous les **jeux d'enregistrements** enfants sont sauvegardés en même temps. Si le **jeu d'enregistrements** actif dépend d'un autre **jeu d'enregistrements**, son parent n'est pas sauvegardé. Tous les **jeux d'enregistrements** enfants formant une sous-arborescence du **jeu d'enregistrements** actif sont sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="de12f-p105">When a hierarchical **Recordset** is saved, all child **Recordsets** are saved along with it. If the current **Recordset** is a child of another **Recordset**, its parent is not saved. All child **Recordsets** that form the subtree of the current **Recordset** are saved.</span></span>

<span data-ttu-id="de12f-125">Lorsque vous rouvrez un **jeu d'enregistrements** à partir de son format de persistance XML, gardez à l'esprit les restrictions suivantes :</span><span class="sxs-lookup"><span data-stu-id="de12f-125">When a hierarchical **Recordset** is reopened from its XML-persisted format, you must be aware of the following limitations:</span></span>

  - <span data-ttu-id="de12f-p106">Si l'enregistrement enfant contient des enregistrements n'ayant pas d'enregistrements parents associés, les lignes correspondantes n'apparaissent pas dans la représentation XML du **jeu d'enregistrements** hiérarchique. Par conséquent, ces lignes sont perdues lorsque le **jeu d'enregistrements** est réouvert à partir de son emplacement de persistance.</span><span class="sxs-lookup"><span data-stu-id="de12f-p106">If the child record contains records for which there are no corresponding parent records, these rows are not written out in the XML representation of the hierarchical **Recordset**. Thus, these rows will be lost when the **Recordset** is reopened from its persisted location.</span></span>

  - <span data-ttu-id="de12f-128">Si un enregistrement enfant est lié à plusieurs enregistrements parent, puis rouvrez le **jeu d’enregistrements**, **l’objet Recordset** enfant peut contenir les enregistrements en double.</span><span class="sxs-lookup"><span data-stu-id="de12f-128">If a child record has references to more than one parent record, then on reopening the **Recordset**, the child **Recordset** may contain duplicate records.</span></span> <span data-ttu-id="de12f-129">Toutefois, ces doublons ne seront visibles que si l’utilisateur travaille directement avec l’ensemble de lignes enfant sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="de12f-129">However, these duplicates will only be visible if the user works directly with the underlying child rowset.</span></span> <span data-ttu-id="de12f-130">Si un chapitre est utilisé pour parcourir le **jeu d’enregistrements** (c’est le seul moyen pour naviguer dans ADO) enfant, les doublons ne sont pas visibles.</span><span class="sxs-lookup"><span data-stu-id="de12f-130">If a chapter is used to navigate the child **Recordset** (that is the only way to navigate through ADO), the duplicates are not visible.</span></span>

