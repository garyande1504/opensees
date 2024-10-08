# ElasticBeamColumn

:::{apidoc="opensees.library.frame.PrismFrame"}

```tcl
element elasticBeamColumn $eleTag $iNode $jNode $A $E $Iz
        $transfTag < -mass $massDens > < -cMass >
```
```tcl
element elasticBeamColumn $eleTag $iNode $jNode $A $E $G
        $J $Iy $Iz $transfTag < -mass $massDens > < -cMass >
```

<hr />
<table>
<tbody>
<tr class="odd">
<td><code class="parameter-table-variable">eleTag</code></td>
<td><p>unique element object tag</p></td>
</tr>
<tr class="even">
<td><p><code class="parameter-table-variable">iNode jNode</code></p></td>
<td><p>end nodes</p></td>
</tr>
<tr class="odd">
<td><code class="parameter-table-variable">A</code></td>
<td><p>cross-sectional area of element</p></td>
</tr>
<tr class="even">
<td><code class="parameter-table-variable">E</code></td>
<td><p>Young's Modulus</p></td>
</tr>
<tr class="odd">
<td><code class="parameter-table-variable">G</code></td>
<td><p>Shear Modulus</p></td>
</tr>
<tr class="even">
<td><code class="parameter-table-variable">J</code></td>
<td><p>torsional moment of inertia of cross section</p></td>
</tr>
<tr class="odd">
<td><code class="parameter-table-variable">Iz</code></td>
<td><p>second moment of area about the local z-axis</p></td>
</tr>
<tr class="even">
<td><code class="parameter-table-variable">Iy</code></td>
<td><p>second moment of area about the local y-axis</p></td>
</tr>
<tr class="odd">
<td><code class="parameter-table-variable">transfTag</code></td>
<td><p>identifier for previously-defined coordinate-transformation
(CrdTransf) object</p></td>
</tr>
<tr class="even">
<td><code class="parameter-table-variable">massDens</code></td>
<td><p>element mass per unit length (optional, default = 0.0)</p></td>
</tr>
<tr class="odd">
<td><p><code class="parameter-table-flag">-cMass</code></p></td>
<td><p>to form consistent mass matrix (optional, default = lumped mass
matrix)</p></td>
</tr>
</tbody>
</table>

:::

## Usage

### Recorders

The valid queries to an elastic beam-column element when creating an
ElementRecorder object are `'force'`.

### Examples

Elastic element with
tag 1 between nodes 2 and 4 with area 5.5, E 100 and Iz 1e6 which uses
transformation 9:

```tcl
element elasticBeamColumn 1 2 4 5.5 100.0 1e6 9; 
```

## Theory

$$
\boldsymbol{N}^{\prime} + \boldsymbol{F} = \boldsymbol{0}
$$

- [With shear](../PrismEulerFrame2d/)
- [Without shear](../PrismShearFrame2d/)


<hr />
<p>Code Developed by: <span style="color:blue"> fmk
</span></p>
