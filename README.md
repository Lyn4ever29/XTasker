<TaskerData sr="" dvi="1" tv="5.0b9m">
	<Task sr="task6">
		<cdate>1516190507883</cdate>
		<edate>1523168628145</edate>
		<id>6</id>
		<nme>直接导入剪贴板的配置</nme>
		<pri>100</pri>
		<Action sr="act0" ve="7">
			<code>888</code>
			<Str sr="arg0" ve="3">%Qii</Str>
			<Int sr="arg1" val="1"/>
			<Int sr="arg2" val="9999"/>
		</Action>
		<Action sr="act1" ve="7">
			<code>410</code>
			<label>先将剪贴板的内容写入到内存卡根目录中为了后续判断正确的文件格式</label>
			<Str sr="arg0" ve="3">%TaskerTmp(%Qii).txt</Str>
			<Str sr="arg1" ve="3">%CLIP</Str>
			<Int sr="arg2" val="0"/>
			<Int sr="arg3" val="0"/>
		</Action>
		<Action sr="act10" ve="7">
			<code>37</code>
			<label>判断是否为任务文件</label>
			<ConditionList sr="if">
				<Condition sr="c0" ve="3">
					<lhs>%Qaa</lhs>
					<op>4</op>
					<rhs>&lt;Task*</rhs>
				</Condition>
			</ConditionList>
		</Action>
		<Action sr="act11" ve="7">
			<code>547</code>
			<label>判断为任务的话，设置后缀为.tsk.xml</label>
			<Str sr="arg0" ve="3">%Houzhui</Str>
			<Str sr="arg1" ve="3">tsk.xml</Str>
			<Int sr="arg2" val="0"/>
			<Int sr="arg3" val="0"/>
			<Int sr="arg4" val="0"/>
			<ConditionList sr="if">
				<Condition sr="c0" ve="3">
					<lhs>%Qaa</lhs>
					<op>4</op>
					<rhs>&lt;Task*</rhs>
				</Condition>
			</ConditionList>
		</Action>
		<Action sr="act12" ve="7">
			<code>410</code>
			<label>最终写入结果</label>
			<Str sr="arg0" ve="3">/sdcard/Tasker/tasks/%TaskerTmp(%Qii) .%Houzhui</Str>
			<Str sr="arg1" ve="3">%CLIP</Str>
			<Int sr="arg2" val="0"/>
			<Int sr="arg3" val="1"/>
		</Action>
		<Action sr="act13" ve="7">
			<code>548</code>
			<Str sr="arg0" ve="3">已经完全导入配置，配置类型为： 任务</Str>
			<Int sr="arg1" val="0"/>
		</Action>
		<Action sr="act14" ve="7">
			<code>38</code>
		</Action>
		<Action sr="act15" ve="7">
			<code>37</code>
			<label>判断是否为场景文件</label>
			<ConditionList sr="if">
				<Condition sr="c0" ve="3">
					<lhs>%Qaa</lhs>
					<op>4</op>
					<rhs>&lt;dmetric*</rhs>
				</Condition>
			</ConditionList>
		</Action>
		<Action sr="act16" ve="7">
			<code>547</code>
			<label>判断为场景的话，设置后缀为.scn.xml</label>
			<Str sr="arg0" ve="3">%Houzhui</Str>
			<Str sr="arg1" ve="3">scn.xml</Str>
			<Int sr="arg2" val="0"/>
			<Int sr="arg3" val="0"/>
			<Int sr="arg4" val="0"/>
		</Action>
		<Action sr="act17" ve="7">
			<code>410</code>
			<label>最终写入结果</label>
			<Str sr="arg0" ve="3">/sdcard/Tasker/scenes/%TaskerTmp(%Qii) .%Houzhui</Str>
			<Str sr="arg1" ve="3">%CLIP</Str>
			<Int sr="arg2" val="0"/>
			<Int sr="arg3" val="1"/>
		</Action>
		<Action sr="act18" ve="7">
			<code>548</code>
			<Str sr="arg0" ve="3">已经完全导入配置，配置类型为： 场景</Str>
			<Int sr="arg1" val="0"/>
		</Action>
		<Action sr="act19" ve="7">
			<code>38</code>
		</Action>
		<Action sr="act2" ve="7">
			<code>415</code>
			<label>读取已保存文件的第二行来判断文件类型</label>
			<Str sr="arg0" ve="3">/sdcard/%TaskerTmp(%Qii).txt</Str>
			<Str sr="arg1" ve="3">2</Str>
			<Str sr="arg2" ve="3">%Qaa</Str>
		</Action>
		<Action sr="act20" ve="7">
			<code>43</code>
		</Action>
		<Action sr="act21" ve="7">
			<code>548</code>
			<Str sr="arg0" ve="3">剪贴板内容不是tasker配置文件，请检查后重新复制</Str>
			<Int sr="arg1" val="0"/>
		</Action>
		<Action sr="act22" ve="7">
			<code>38</code>
		</Action>
		<Action sr="act23" ve="7">
			<code>406</code>
			<label>删除内存卡根目录文件</label>
			<Str sr="arg0" ve="3">/sdcard/%TaskerTmp(%Qii).txt</Str>
			<Int sr="arg1" val="0"/>
			<Int sr="arg2" val="0"/>
		</Action>
		<Action sr="act24" ve="7">
			<code>548</code>
			<Str sr="arg0" ve="3">现在直接在Tasker里导入，文件名为 %TaskerTmp(%Qii) .%Houzhui</Str>
			<Int sr="arg1" val="0"/>
		</Action>
		<Action sr="act3" ve="7">
			<code>548</code>
			<Str sr="arg0" ve="3">%Qaa</Str>
			<Int sr="arg1" val="0"/>
		</Action>
		<Action sr="act4" ve="7">
			<code>37</code>
			<ConditionList sr="if">
				<bool0>Or</bool0>
				<bool1>Or</bool1>
				<Condition sr="c0" ve="3">
					<lhs>%Qaa</lhs>
					<op>4</op>
					<rhs>&lt;Profile*</rhs>
				</Condition>
				<Condition sr="c1" ve="3">
					<lhs>%Qaa</lhs>
					<op>2</op>
					<rhs>&lt;dmetric*</rhs>
				</Condition>
				<Condition sr="c2" ve="3">
					<lhs>%Qaa</lhs>
					<op>4</op>
					<rhs>&lt;Task*</rhs>
				</Condition>
			</ConditionList>
		</Action>
		<Action sr="act5" ve="7">
			<code>37</code>
			<label>判断是否为配置文件</label>
			<ConditionList sr="if">
				<Condition sr="c0" ve="3">
					<lhs>%Qaa</lhs>
					<op>4</op>
					<rhs>&lt;Profile*</rhs>
				</Condition>
			</ConditionList>
		</Action>
		<Action sr="act6" ve="7">
			<code>547</code>
			<label>判断为配置文件的话，设置后缀为.scn.xml</label>
			<Str sr="arg0" ve="3">%Houzhui</Str>
			<Str sr="arg1" ve="3">prf.xml</Str>
			<Int sr="arg2" val="0"/>
			<Int sr="arg3" val="0"/>
			<Int sr="arg4" val="0"/>
		</Action>
		<Action sr="act7" ve="7">
			<code>410</code>
			<label>最终写入结果</label>
			<Str sr="arg0" ve="3">/sdcard/Tasker/profiles/%TaskerTmp(%Qii) .%Houzhui</Str>
			<Str sr="arg1" ve="3">%CLIP</Str>
			<Int sr="arg2" val="0"/>
			<Int sr="arg3" val="1"/>
		</Action>
		<Action sr="act8" ve="7">
			<code>548</code>
			<Str sr="arg0" ve="3">已经完全导入配置，配置类型为： 配置文件</Str>
			<Int sr="arg1" val="0"/>
		</Action>
		<Action sr="act9" ve="7">
			<code>38</code>
		</Action>
	</Task>
</TaskerData>
